# interfaces

* uma interface declara métodos que deverão ser implemetnados pelas classes concretas
* por padrão, mesmo que não sejam definidos como públicos e abstratos, todos os métodos são públicos e abstratos
  * **ou seja**, não é possível alterar os seus modificadores de visibilidade
* toda classe que implementa uma interface deve implementar todos os seus métodos
 
* se uma classe pai implementa uma método, e uma classe filha implementa outro, e a classe filha diz implementar uma interface que define os dois métodos, não há a necessidade de sobrescrever o método do pai na filha, desde que ambos sejam publicos, pois não é possível restringir a visibilidade
* de modo similar às classes abstratas, se uma classe pai nao implementa um dos métodos da interface, um dos filhos deverá fazê-lo
* se um dos filhos implementar a interface e nao implementar um dos métodos, deverá ser decalrado como abstrato

* um classe pode implementar diversas interfaces
* uma interface pode herdar de outra
* aliás, uma interface admite herança múltipla e pode herdar de múltiplas interfaces, pois não está na verdade herdando comportamento, mas compondo-o
* uma interface nunca implementa outra interface

* é possível declarar constantes em uma interface
* mesmo que não sejam adicionados os modificadores static final, toda variável declarada em uma interface é estática e final
* 
