# estrutura de uma classe

* a declaração do pacote é opcional, mas deve ser a primeira coisa, e só pode haver um
* as importações vêm depois do pacote, são opcionais e pode haver mais de uma
* a declaração da classe deve vir logo a seguir
* comentários podem acontecer em qualquer lugar, inclusive antes da declaração do pacote
* até mesmo um arquivo vazio compila
* um arquivo com a declaração de um pacote, ou só com imports, ou só com pacote e imports também compila
* 

# comentários
* comentários podem ser feitos com barras duplas, barra e asterisco e barra asterisco asterisco (javadoc)
* pode haver comentários inclusive entre a palavra classe e o nome dela, ou entre os modificadores

# organização em pacotes e diretórios e a ideia de namespace

# estrutura de uma classe

* uma classe pode ter variáveis de instancia e classe, métodos e construtores
* uma classe pode ter o mesmo nome de uma variável ou de um método
* **em um arquivo java só pode haver a declaração de 1 único tipo público**
* **pode -contudo- haver mais de um tipo se forem públicos**
* **se o tipo for público, ele deve ter o mesmo nome do arquivo**
* um contrutor não retorna nada e tem o mesmo nome da classe
* é possível terminar um construtor com um return vazio
* no caso de múltiplas classes dentro de um mesmo arquivo, o pacote ainda deve ser a primeira declaração, seguida dos imports

# interfaces

* interfaces aceitam constantes
* não é possível declarar outros tipos de variáveis que não sejam **final**
* mesmo que não se declare como final, ela é final
* **por padrão, toda variável de uma interface é estática, pois não é possível instanciar uma interface**
* todo método de uma interface é abstrato e público
* mesmo que ue nao escreva public e abstract, ele é público e abstrato
* 
