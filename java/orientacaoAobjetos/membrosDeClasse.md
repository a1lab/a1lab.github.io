# Membros estáticos

* o modificador _static_ determina que o membro (método ou atributo) pertence à toda a classe de objetos e não a uma instância específica
* não é necessário ter uma instância para acessar tais valores, desde que sua visibilidade seja pública
  * em outras palavras: mesmo que nenhum objeto tenha sido instanciado, é possível acessar tais membros
* É possível acessar um atributo estático por meio de uma instância, ou por meio do nome da classe

```java
class Pessoa{
  static int idade = 18;
  public static void main(String[] args){
    Pessoa p = new Pessoa();
    p.idade = 20;
    Pessoa.idade = 21;
  }
}
```

* É possível acessar um membro estático por meio de um método não estático
* Não é possível acessar um membro de instância por meio de um método de classe, pois o método de classe não sabe a qual instância o membro se refere
* Nesse caso, o código não compila

```java
    Carro c = new Carro();
    int i = c.getTotalDeCarros();

```

* Suponha que **getTotalDeCarros()** seja um método estático. Nesse caso, o código compila, mas pode levar a um equivoco
* Por isso, é uma boa prática usar o nome da classe para acessar membros estáticos ao invés de usar instâncias

* não existe sobrecarga nem sobrescrita de métodos estáticos e não estáticos
* por isso, um método estático e outro de instância nunca podem ter o mesmo nome, nem quando um pertence a uma classe; e outro a um subtipo

```java

class A {
    static void a() { // não compila
    }
    void a() { // não compila
    }
}

class B {
    static void a() {
    }
}
class C extends B {
    void a() { // não compila
    }
}

```

* a declaracao de uma variavel estática pode invocar outras variáveis estáticas e métodos estáticos
* a declaracao de uma variável de instancia pode invocar tanto métodos e atributos de instancia, quanto de calsse
* nao é possível usar o _this_ em um contexto estático, ou seja, dentro de um método de classe
* 
