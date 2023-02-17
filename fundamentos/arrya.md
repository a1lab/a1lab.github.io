# declarando arrays

```java
  int[] idades;
  double pesos[];
  long []numeros;
  long[]tamanhos;
```

* Um _array_ é um objeto que guarda vários elementos de um mesmo tipo
* A inicilização de um array é feita por meio do operador **new**
* Ao inicializar um array, deve-se informar sua capacidade: quantos elementos ele vai guardar

```java
  int[] idades = new int[]10];
```

* É possível inicializar um array, fornecendo a ele uma capacidade 0 ou negativa, sem que isso cause um erro de compilação
* Contudo, em tempo de execução, isso vai causar um **NegativeArraySizeException**


* Também é possível inicializar o array da seguinte forma:

```java
  int[] idades = new int[]{18,25,32};

  Cliente[] clientes = new Cliente[]{
    new Cliente(),
    new Cliente()
  };
```

* Esse tipo de inicialização só funciona se o _array_ for declarado e inicializado ao mesmo tempo, ou seja, na mesma instrução.

* o acesso a um array é feito por seu índice, iniciando em zero e terminando em (tamanho-1)

* foreach:

```java
  int[] idades = new int[]{1,2,3};
  for(int idade: idades){
    System.out.println(idade);
  }
```

* ao inicializar um array, o valor de todos os seus elementos é o valor _default_ do tipo do _array_
* se for um _array_ de tipos de referencia, o valor default é nulo, de modo que, ao tentar acessar um membro de um elemento não inicializado, o sistema causará um **NullPointerException**

* Em um array de referencias, é possível alocar subclasses do tipo do _array_

```java
  class Pessoa{}
  class PessoaFisica extends Pessoa{}

  public static void main(String[] args){
    Pessoa[] pessoas = new Pessoa[2];
    pessoas[0] = new PessoaFisica();
  }
```

# importante

* Uma vez que o array de objetos é sempre baseado em referências, lembre-se que um objeto não será copiado, mas somente sua referência passada:

```java
Cliente guilherme = new Cliente();
guilherme.setNome("guilherme");

Cliente[] clientes = new Clientes[10];
clientes[0] = guilherme;

System.out.println(guilherme.getNome()); // guilherme
System.out.println(clientes[0].getNome()); // guilherme

guilherme.setNome("Silveira");

System.out.println(guilherme.getNome()); // silveira
System.out.println(clientes[0].getNome()); // silveira
```


