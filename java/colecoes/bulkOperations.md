# bulkOperations

* containsAll retorna verdadeiro se todos os elementos contidos na coleção passada como parâmetro estiverem também contidos na coleção original
  * se a coleção original tiver mais elementos que a coleção parametro também retorna verdadeiro 
* addAll adiciona todos os elementos
  * o que acontece se a coleção não admitir duplicatas e houver um elemento repetido? os demais são adicionados na coleçõa? ocorre uma exceção?
* removesAll 
* retainsAll remove da coleção objetivo todos os elementos que estão contidos na coleção especificada
* clear remove todos os elementos

* os métodos abaixo criam uma instância de **set** por meio da **factory** Collections.singleton e utilizam-no como parâmetro para remover o elemento **e** ou os elementos nulos da coleção objetivo

```java
c.removeAll(Collections.singleton(e));
c.removeAll(Collections.singleton(null));
```

