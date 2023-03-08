# Tipos de variáveis

Variáveis são elementos que guardam valores durante o tempo de execução do programa. 
Como o próprio nome já diz, esses valores podem ser alterados, por expressões, operações e funções.
No sentido amplo, variáveis abrangem também as constantes, que -uma vez declaradas e inicializadas- não podem ter seus valores alterados.
Java define 4 tipos de variáveis: variáveis locais e parâmetros servem para guardar estados temporários; variáveis de instância e de classe, para representar propriedades de classes e objetos, de forma mais duradoura.

- **Variáveis locais** 
    - Declaradas dentro de um método (entre as chaves que delimitam seu corpo).
    - Servem para guardar um estado temporário.
    - Seu escopo está limitado ao corpo do método no qual foram declaradas.
    - Seu estado é protegido internamente pelo método e só pode ser alterado indiretamente por parâmetros desse método.
- **Parâmetros**
    - Declaradas na assinatura de um método.
    - Seu escopo também se resume ao corpo do método.
    - Seu estado é definido no momento em que o método é invocado e seu valor é estabelecido por quem o invocou.
- **Variáveis de instância**
	- Também chamadas de campos não-estáticos.
    - Declaradas dentro de uma classe (entre as chaves que delimitam seu corpo).
    - Podem ser acessadas diretamente por quaisquer outros membros (campos e métodos) da mesma classe, mesmo que tenha a visibilidade mais restritiva (*private*).
    - O acesso direto por membros de outras classes depende de sua visibilidade.
        - Se a visibilidade for *public*, poderá ser acessada de qualquer outra parte da aplicação.
        - Se *default*, poderá ser acessada de qualquer outra classe contida no mesmo pacote da classe na qual foi declarada.
        - Se *protected*, de qualquer subtipo da classe na qual foi declarada.
    - Guardam o estado de uma instância da classe, enquanto o objeto existir na memória da aplicação.
    - Cada instância da classe pode guardar valores diferentes em seus campos não-estáticos.
- **Variáveis de classe**
    - Também chamadas de campos estáticos.
    - Declaradas também no corpo de uma classe.
    - Diferem-se das variáveis de instância em virtude do modificador *static*.
    - Guardam o estado da classe, durante toda a execução do programa.
    - Todas as instâncias da guardam o mesmo valor.
    - Mesmo que nenhuma instância tenha sido criada, a classe mantém os valores de seus campos estáticos, tais quais foram inicializados. 	

