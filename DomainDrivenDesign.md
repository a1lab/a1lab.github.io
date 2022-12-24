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

![Domain-Driven-Design-Overview-of-a-Layered-Architecture](https://user-images.githubusercontent.com/2974552/209432372-a62ca9eb-6558-4b8f-9ace-966df5120660.png]

## Linguagem ubíqua

* Mesmos termos do glossário, devem constar no projeto, escopo, código, etc.
* Casos de uso devem ser mapeados em classes específicas, que realizam ações
* 

* Os contextos delimitados de uma aplicação DDD podem evoluir para microsserviços separados.
* A vantagem de separar em microsserviços é que cada um deles pode ser implementado com tecnologias diferentes, mantido em repositórios diferentes, com uma infraestrutura diferente, e se um deles cair, os outros podem continuar funcioinando.
* 
