# Interface Iterator

* Nem todas as coleções em Java são ordenadas, ou seja, em alguns casos não é possível obter um elemento a partir de seu índice
* Por esse motivo, a própria interface Collection extende a interface Iterable, o que permite invocar um Iterator, para percorrer seus elementos
* Embora seja possível usar o Iterator em uma coleção ordenada, não há necessidade

## hasNext

* o método **hasNext** retorna verdadeiro se existe um elemento a ser percorrido no iterador

## next

* o método **next** passa para o próximo elemento

## remove

* remove o elemento atual do iterator

## enhanced-for

* Os dois trechos de código abaixo produzem o mesmo efeito

```java
    Collection<String> strings = new ArrayList<String>();
    for (String atual : strings) {
        System.out.println(atual);    
    }
```

```java
    Collection<String> strings = new ArrayList<String>();
    Iterator<String> iterator = strings.iterator();
    while (iterator.hasNext()) {
        String atual = iterator.next();
        System.out.println(atual);
    }
```

