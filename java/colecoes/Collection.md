* uma **collection** é usada para dar maior abstração a um agrupamento de elementos
* apropriada para casos em que a ordem a as redundancias nao importam
* contém os seguintes métodos
  * size(): int retorna a quantidade de elementos contidos na coleção
  * isEmpty(): boolean retorna verdadeiro se não houver elementos na coleção; falso, caso contrário
  * contains(Object element): boolean retorna verdadeiro se o elemento indicado pertencer à coleção
  * containsAll(Collection<?> c): boolean
  * add(E element): boolean retorna verdadeiro se for possível adicionar o elemento à coleção
  * addAll(Collection<?> c): boolean
  * remove(E element): boolean retorna verdadeiro se for possível remover o elemento da coleção
  * removeAll(Collection<?> c): boolean
  * iterator(): Iterator<E> retorna um objeto do tipo iterator
  * retainAll(Collection<?> c) boolean remove todos os elementos na intersecção entre as coleções
  * clear(): void remove todos os elementos
  * toArray
  * stream
  * parallelStream
  
* Como a interface estabelece métodos para todos os tipos de implementação, o método add pode não fazer sentido em alguns casos
* add só retorna falso se houver uma tentativa de adicionar um elemento repetido a uma implementação que não admite redundâncias
* da mesma forma, o remove só retorna false se houver a tentativa de remover um elemento de uma implementação que só permite a remoção das pontas
* o iterator também só faz sentido para coleções que não são ordenadas
  
# percorrendo uma coleção

* há três meios para percorrer uma coleção: com um laço, com um iterator, ou com um stream
* o for each permite percorrer os elementos, mas nao permite modificar a coleçaõ original, nem acessar os elementos pelo indice, mesmo que a coleção seja ordenada

  
