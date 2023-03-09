# iterator

* um iterator permite atravessar uma coleção e remover elementos se necessário
* o método **hasNext** retorna verdeiro se houver mais um elemento acessível na coleção
* o método **remove** remove o último elemento retornado pelo método **next**
  * o método **remove** só pode ser chamado uma vez para cada chamada do método **next**, senão ele lança uma exceção
* usar um iterator é uma forma segura de alterar a coleção enquanto a percorre
* também é mais apropriado usar um iterator se for necessário percorrer mais do que uma coleção em paralelo

```java
static void filter(Collection<?> c) {
    for (Iterator<?> it = c.iterator(); it.hasNext(); )
        if (!cond(it.next()))
            it.remove();
}
```

