# arrays de referencia

* em um array de tipos de referencia são guardados apenas os tipos de referencia do array
  * não é possível guardar outros tipos de referência, nem primitivos
  * a única exceção é guardar subtipos do tipo do array, ou implementações de interfaces -como no exemplo abaixo.
* ao inicializar um array de tipo de referencia, todas as posições são inicializadas com null, que é o valor _default_ para os tipos de referência

```java
Pessoa[] pessoa = new Pessoa[10];
pessoa[0] = new PessoaFisica();//PessoaFisica extends Pessoa implements PessoaJuridicaDeDireitoPublico
```

* ao associar um objeto a uma posição em um array, alterá-la causará uma alteração na referência do array

* no caso de arrays de tipos de referencia é possível fazer _casting_, ao contrário dos arrays de tipos primitivos

```
String[] nomes = new String[10];
Object[] objetos = nomes;
```

* perceba que o contrário não é possível, pois String é filha de Object, mas o contrário não é verdadeiro

```java
Object[] objetos = new Object[10];
String[] nomes = objetos;
```

> ClassCastException

* todo array herda de object

* é possível declarar um array sem inicializá-lo
* também é possível declará-lo em uma linha e inicializá-lo em outra, ou fazer ambos na mesma linha
* um array pode ter tamanho zero
* também é possível declarar e inicializar de forma compacta, fornecendo seus valores
* não é possível inicializar um array sem declarar seu tamanho

```java
int x[];
int y[] = new int[1];
x = new int[1];
int[] q = {1,2,3};
int z = new int[];//nao compila
```

> Unresolver compilation problem: Variable must provide either dimension expressions or an array initializer

## arrays multi dimensionais

```java
// Um array de duas dimensões.
int[][] tabela;

// Um array de três dimensões.
int[][] cubo[];

// Um array de quatro dimensões.
int[] [][]hipercubo[];

// Perceba que as dimensões podem ser definidas do lado 
// esquerdo ou direito da variável.
```

```java
// Inicializando a primeira dimensão com 10 e a segunda com 15
tabela = new int[10][15];

// Inicializando a primeira dimensão com 10 e deixando as outras
// para serem iniciadas depois
cubo = new int[10][][];

// Inicializando com valores
int[][] teste = new int[][]{{1,2,3},{3,2,1},{1,1,1}};
```

```java

int[][] estranha = new int[2][];
estranha[0] = new int[20];
estranha[1] = new int[10];
for(int i=0;i<estranha.length;i++) {
    System.out.println(estranha[i].length); // imprime 20 e 10
}
```
