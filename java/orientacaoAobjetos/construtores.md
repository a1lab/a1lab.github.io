# construtores

* um construtor é um membro da classe que não tem um tipo de retorno, tem o mesmo nome da classe e devolve uma instancia da classe

* todo tipo de referencia criado pelo dev herda de object, mesmo que tal declaração não seja explicita
* dessa foram, toda classe possui um construtor padrão, que não recebe argumentos e tem a mesma visibilidade da classe
* caso um construtor seja decalrado explicitamente, o construtor padrao deixa de existir
* dentro de um construtor é possível acessar outros membros tanto de classe, quanto de instancia
* como não é obrigatório inicializar as variáveis de instancia, ao acessá-las no construtor, pode ocasionar um nullpointerexception

* construtores podem ter qualquer tipo de modificador de visibilidade
* é comum ter um construtor privado e um método estático para criar seu objeto (padrão builder ou factory)
* é possível ter um método que tem o mesmo nome da classe, retornando void.
  * nesse caso, não se trata de um construtor, mas de um simples método
  *  

* construtores também podem ser sobrecarregados
* um construtor pode chamar outro, por meio da palavra reservada _this_
* a chamada _this_ deve ser sempre a primeira dentro do construtor
* não é possível ter duas chamadas this
* a chamada this pode envolver outro método, desde que nao seja de instancia, pois o objeto ainda nao foi construido

```java

class Teste {
    public Teste() {
        System.out.println("construtor simples");
    }
    public Teste(int i) {
        this();
    }
    public Teste(String s) {
        this(s, s);  // não compila, loop
    }
    public Teste(String s, String s2) {
        this(s); // não compila, loop
    }
}
```

* construtores sobrecarregados seguem as mesmas regras dos métodos
* quando existem dois construtores/metodos, sendo que um tem zero parametros e outro tem um varargs, ao invocá-lo sem nenhum parâmetro, Java vai invocar o construtor/metodos sem parametros, ao invés de invocar o com varargs

```java

void desativa(Cliente... clientes) {
    System.out.println("varargs");
}
void desativa() {
    System.out.println("sem argumento");
}
void metodo() {
    desativa(); // imprime sem argumento
}
```

