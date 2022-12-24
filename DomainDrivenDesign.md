# Domain Driven Design

* Criado por Eric Evans
* Domain-Driven Design: Tackling Complexity in the Heart of Software. By Eric Evans 2003
* Clean Architecture. By Robert Cecil Martin 2017
* Microsserviços foram criados em 2011 em um work de Dr Peter Rogers
> Desenvolver _software_ orientado ao domínio, ao invés da tecnologia
* Características
  * Contexto delimitado
  * Linguagem ubíqua
  * Foco no domínio
  * Blocos de construção
    * Entidades (persistentes ou transientes)
    * Value Objects (não existem isoladamente; dependem da existencia de uma entidade)
    * Repositories
    * Feactories
    * Services 

No DDD, a camada de domínio conhece a camada de infraestrutura; ao passo que no clean architecture, o domínio conhece apenas a interface da infra, mas não sua implementação.

![Domain-Driven-Design-Overview-of-a-Layered-Architecture](https://user-images.githubusercontent.com/2974552/209432372-a62ca9eb-6558-4b8f-9ace-966df5120660.png)

## Linguagem ubíqua

* Mesmos termos do glossário, devem constar no projeto, escopo, código, etc.
* Casos de uso devem ser mapeados em classes específicas, que realizam ações

## _Aggregates_

* Invariantes são restrições do domínio dos dados
* Uma entidade deve sempre mantes um estado consistentes, ao invés de validar o estado após sua criação
* Invariantes devem ser colocar dentro das próprias classes de domínio
* Uma entidade é composta por um conjunto de value objects
  * Essa entidade da qual os VOs dependem é o _aggregate root_
* Os objetos agregados devem ser protegidos pela raíz. Ou seja, não deve ser possível adicionar uma agregação sem passar pela raíz, na qual ficam as invariantes.
* Persistência deve ser feita pelo _aggregate root_.

> https://martinfowler.com/bliki/DDD_Aggregate.html

<!-- 

Dada uma classe Aluno{List<String> telefones}, em que um aluno só pode ter no máximo 5 telefones, como prevenir que isso aconteça no banco de dados?

Ao colocar 5 colunas, a tabela pode se tornar esparça. Ao separar em uma nova tabela, não há limitação para que um aluno tenha mais do que 5 telefones.

A validação deve ser feita na aplicação. Ou por meio de triggers/procedures

-->

## Eventos

* Entidade, VOs, utilitarios, exceções e eventos de um determinado contexto devem ficar no mesmo pacote
* um evento deve implementar uma interface evento. No caso do spring, eles estendem de ApplicationEvent
* O evento customizado deve conter os dados necessários ao ouvinte do evento
* O evento deve carregar apenas a chave primária dos objetos relacionados, para evitar expor outros detalhes de implementação

## Contextos delimitados

<!--
Como separar os contextos usando pacotes do maven ou módulos do java 9?
-->

* Os contextos delimitados de uma aplicação DDD podem evoluir para microsserviços separados.
* A vantagem de separar em microsserviços é que cada um deles pode ser implementado com tecnologias diferentes, mantido em repositórios diferentes, com uma infraestrutura diferente, e se um deles cair, os outros podem continuar funcioinando.
* O que acontece se um contexto compartilha um VO de outro contexto?
* Pode-se usar um contexto compartilhado, ou duplicar o código. Também é possível gerar as classes em tempo de compilação, usando swagger

> https://martinfowler.com/bliki/BoundedContext.html

## Shared Kernel

* Entidades e VOs compartilhados devem ficar em um pacote compartilhado (shared)
* cada contexto deve ser colocado em um pacote; e dentro de cada contexto deve haver um pacote para os casos de uso
* os casos de uso devem ser ouvintes de evento
* contextos delimitados podem ter dependências apenas para o contexto compartilhado

> https://maiconheck.medium.com/domain-driven-design-os-building-blocks-parte-3-domain-subdomains-e-bounded-contexts-a51d5a9d9851

```java
interface Evento{
  LocalDateTime momento();
  TipoEvento tipo();
  Map<String, Object> informacoes();
}

class AlunoMatriculado implements Evento{
  private final CPF cpfDoAluno;
  private final LocalDateTime momento;
}

class GeraSeloAlunoNovato extends Ouvinte{
  protected void reageAo(Evento evento){
    CPF cpfDoAluno = (CPF) evento.informacoes().get("cpf");
    Selo novato = new Selo(
  }

  protected boolean deveProcessar(Evento evento){
    return evento.tipo == TipoEvento.ALUNO_MATRICULADO;
    //isso evita um instanceof que exigiria a classe AlunoMatriculadoEvento do contexto delimitado
  }
}
```
