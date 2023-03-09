# Coleções

* uma coleção também é chamada de container
* é um objeto que agrupa multiplos elementos em uma única unidade
* representam um grupo natural
* sao usados apra armazenar, recuperar, manipular e comunicar dados agregados

* todas as coleções java seguem a mesma interface, o que permite uma manipulação uniforme
* a api java contém implementações de tais interfaces
* a api também contém algoritmos que permitem busca, ordenação, inserção e remoção de elementos
* esses algortimos sao polimorficos e podem ser usados em qualquer implementacao de coleção

# beneficios

* aumenta a eficiencia sobre estruturas de dados
* evita reescrever codigo para manipular estruturas
* permite interoperabilidade entre apis
* permite reuso

# interfaces da api


![colls-coreInterfaces](https://user-images.githubusercontent.com/2974552/224036067-0e4ce1e3-4da3-4a0a-8763-0affea5268a1.gif)

* um mapa (e um mapa ordenado) não são coleções
* as itnerfaces da api de coleções são genericas, ou seja, podem ser aplicadas a quaisquer tipos
* determinar o tipo durante a instanciacao permite identificar erros em tempo de compilacao


* uma coleção é a raiz da hierarquia e representa um agrupamento de elemnetos
  * alguns tipos de coleções permitem elementos duplicados, outros nao; alguns sao ordenados, outros nao
* um **set** é uma coleção que nao admite elementos duplicados
* uma **list** é uma coleção ordenada, que admite elementos repetidos
* uma **queue** é uma coleção ordenada, que admite elementos repetidos, e só admite a inserção de elementos na causa; e remoção da cabeça
* um **deque** é parecido com uma fila, mas admite inserção e remoção em ambas as pontas
* um **map** mapeia elementos (sic). Para acessá-los é necessaário fornecer suas chaves. Cada chave pode armazenar multiplos elementos repetidos, mas as chaves nao podem ser repetidas
* um **sortedSet** é um conjunto que mantém seus elementos ordenados
* um **sortedMap** é um mapa que mante´m suas chaves ordenadas
