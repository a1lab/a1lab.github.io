# super

* métodos e contrutores podem ser sobrecarregados
* um construtor sobrecarregado sempre deve chamar um construtora da classe mãe primeiro
* para isso, deve usar o operador **super**
* se nenhum construtor da classe mãe for chamado explicitamente, o compilador coloca uma chamada implícita ao construtor sem parametros

# this

* para invocar outro construtor da própria classe, é possível usar o operador **this**

* se houver uma chamada aos construtores usando **this** ou **super**, essa deve obrigatoriamente ser a primeira instrucao do construtor

# this e variáveis membro

* quando variáveis locais de um método (ou parâmetros) tem o mesmo nome de variáveis membro, para acessar as variáveis membro, é necessário usar **this**
* this pode ser usado para acessar atributos públicos, default ou protected das classes pai
* tentar acessar uma variável local com this não compila
* caso exista uma variável membro com o mesmo nome na classe filha e outra na classe pai, é possível acessar uma com **this**, e outra com **super**
  * se nao declararmos nem this, nem super, o compilador fará o binding à variável da classe filha
* **this** é opcional para acessar variáveis membro da própria classe

# membros estáticos

* contextos estáticos não possuem nem this, nem super

