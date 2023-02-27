# ArrayList

* um array list é uma lista que utiliza um array como estrutura, o que a permite ter tempo de acesso constante na leitura
* um ArrayList herda diversos métodos abstratos e concretos de List e consequentemente de Collection

## add

* para adicionar um elemento em uma posição específica add(posicao, valor);

## addAll

* add adiciona um elemento no final da lista
* o elemento a ser inserido deve ser do mesmo tipo que o arraylist
* add retorna verdadeiro se a lista foi alterada
* como o método é herdado de Collection, se o tipo de coleção não permitir duplicatas, o método add retorna falso
  * no caso de arraylist, o método sempre retornará verdadei
* também é possível adicionar um elemento em uma posição determinada, fornecendo dois parâmetros, o elemento e a posição
* todos os elementos com índice maior do que o índice informado serão shiftados para a direita
* se a posição fornecida for maior do que o tamanho da lista, o método lança um ArrayOutOfBoundsException

# set

* serve para sobrescrever o elemento de determinado índice

## remove

* se o arraylist tiver dois elementos repetidos, o método remove remove apenas um deles

```java

import java.util.ArrayList;
class A {
    public static void main(String[] args) {
        ArrayList<String> c = new ArrayList<String>();
        c.add("a");
        c.add("a");
        System.out.println(c.remove("a"));
        System.out.println(c.size());
    }
}
```

b ={a, b}
c = {c, d}
a = {a,b,c,d}


## contains
## size
## toArray

* o método toArray sem argumentos retorna um array de objects

```java

import java.util.ArrayList;
class A {
    public static void main(String[] args) {
        ArrayList<String> l = new ArrayList<String>();
        l.add("a");
        l.add("b");
        l.add(1,"amor");
        l.add(3,"baixinho");
        System.out.println(l);
        String[] array = l.toArray();
        System.out.println(array[2]);
    }
}
```

## get
## indexOf

* retorna o índice em que o elemento for primeiro encontrado

## lastIndexOf

* retorna o índice em que o elemento foi encontrado por último

# equals

```java
public static void main(String[] args) {
		Collection<String> colecao1 = new ArrayList<>();
		Collection<String> colecao2 = new ArrayList<>();
		
		colecao1.add("felipe");
		colecao2.add("felipe");
		
		System.out.println(colecao1.equals(colecao2));
	}
```

* é importante salientar que, como um arraylist trabalha com um array internamente, ao adicionar um objeto nessa coleção, apenas estamos referenciando-o, de modo que ao alterar o objeto original, ao acessá-lo pelo arrayList, essa referência também será alterada

# observar esta situacao

```java

import java.util.ArrayList;
class A {
    public static void main(String[] args) {
        ArrayList<String> ss = new ArrayList<String>();
        ss.add("a");
        ss.add("b");
        ss.add("c");
        ss.add("d");

        for(String s:ss){
            if(s.equals("c")) s = "b";
            else if(s.equals("b")) s= "c";
        }
        for(String s:ss) System.out.println(s);
    }
}
```
