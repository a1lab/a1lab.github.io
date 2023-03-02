# operador de atribuição

* o operador de atribuição **=** permite guardar um valor literal em uma variável
* a atribuição de valores exige um valor literal e uma variável, ambos do mesmo tipo
  * excepcionalmente é possível atribuir a um tipo primitivo "maior" ou a um super tipo de referência
  * é possível atribuir um valor literal inteiro a um byte, desde que não ultrapasse os limites  do tipo
  * também é possível atribuir um valor literal inteiro  a um char, desde que positivo, pois não existem índices negativos na tabela do char

* na atribuição de valores, a passagem de parametros é por referencia e não por copia

# operadores de incremento e decremento
* se aplicam somente a variáveis
* nao se aplicam a literais, nem a métodos
* diferença entre pré e pós: 

# operadores aritméticos

* a manipulação dos valores contidos nas variáveis pode ser feita por meio de operadores aritméticos
* +,-,*,/,%
* o resultado de uma operação é sempre do tipo mais abrangente

```java
int daquiCincoAnos2 = idade + anos; //nao compila, pois o lado direito da expressão é do tipo long
```

```java

byte b = 1;
short s = 2;

// devolve no mínimo int, compila
int i = b + s; 

// não compila, ele devolve no mínimo int
byte b2 = i + s; 

// compila forçando o casting, correndo risco de perder 
// informação
byte b2 = (byte) (i + s); 

```

* ao dividir um número por zero, o compilar lança um NonANumber

```java

int i = 200;
int v = 0;

// compila, mas exception
System.out.println(i / v); 

// compila e roda, infinito positivo
System.out.println(i / 0.0); 

```

## operadores de comparação

* == igual, != diferente, > maior, < menor, >= maior ou igual, <= menor ou igual
* uma comparação sempre devolver um valor booleano: verdadeiro ou falso
* toda comparação que envolve valores numéricos não considera o tipo, apenas o valor

```java
  System.out.println(1 == 1.0);// compila e imprime true
```

> true

* valores booleanos e os tipos de referencia só podem usar os operadores de comparação de igualdade e desigualdade
  * char pode usar operadores relacionais, visto que ele guarda um valor numérico intrinséco
 
# operadores lógicos

* nada a acrescentar exceto a questão da avaliação dos dois lados da expressão booleana
* se o lado direito não for avaliada (em razao de short circuiting), e essa expressao fizer uma alteração em alguma variável, isso pode gerar um efeito colateral indesejado

# operadores de incremento e decremento

* o incremento pode ser pós ou pré
* é possível usar todos os operadores aritméticos em uma única linha, inclusive o módulo

```java
int j = 0;
int i = (j++ * j + j++);
System.out.println(i);
System.out.println(j);
```

```java
i = (0 * j + j++); // j vale 1
i = (0 * 1 + j++); // j vale 1
i = (0 * 1 + 1); // j vale 2
i = 1; // j vale 2
```

```java
int a = 15, b = 20, c = 30;
a = b = c; // b = 30, portanto a = 30
```
```java
int a = 15, b = 20, c = 30;
a = (b = c + 5) + 5; // c = 30, portanto b = 35, portanto a = 40
```

## operador ternário

A estrutura do operador ternário é a seguinte:

variável = teste_booleano ? valor_se_verdadeiro : valor_se_falso;

```java

int i = 5;
System.out.println(i == 5 ? "verdadeiro": "falso");// verdadeiro
System.out.println(i != 5 ? 1: 2);                   // 2

String mensagem = i % 2 == 0 ? "é par" : "é ímpar";

## precedencia

Precedência
Não é necessário decorar a precedência de todos operadores do Java, basta saber o básico, que primeiro são executados pré-incrementos/decrementos, depois multiplicação/divisão/mod, passando para soma/subtração, depois os shifts (<<, >>, >>>) e, por último, os pós-incrementos/decrementos.

As questões da certificação não entram em mais detalhes que isto.
```

