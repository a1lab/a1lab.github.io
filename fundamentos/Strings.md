# String Buffer

* Em um string buffer, o objeto é mutável, ao contrário da própria string
* é possível inicializar um string buffer, informando o tamanho do array utilizado internamente

```java
StringBuilder sb3 = new StringBuilder(5);
System.out.println(sb3); // linha em branco
System.out.println(sb3.length()); // 0
sb3.append("abcdef");
		System.out.println(sb3);
		System.out.println(sb3.length());

```

* mesmo que o array tenha sido inicializado com 5 espaços, é possível alterar seu tamanho
* length retorna a quantidade de caracteres da string contida no objeto
* capacity retorna a quantidade de espaços de memória do array interno

# String Builder

* StringBuilder e StringBuffer têm a mesma interface
* A diferença é que StringBuffer é thread-safe e StringBuilder, não
* Por esse motivo, os locks utilizados na StringBuffer tornam ela mais lenta
* Ao concatenar strings com o operador **+**, java trunca para uma stringbuilder e depois devolver uma string

* Para concatenar, basta usar o método append, que retorna o próprio objeto, o que permite encadear concatenações
* Para inserir em um lugar específico, é necessário usar o método insert, fornecendo como primeiro parâmetro a posição do elemento
* O método delete remove os caracteres contidos no intervalo informado
* Reverse reverte a ordem dos caracteres
* toString converte para um string
* o método substring não altera o valor do stringbuilder/buffer, mas retorna um novo objeto do tipo string, com o conteúdo do intervalo informado

# string são imutáveis

```java
    String s = "caelum";
    s.toUpperCase();
    System.out.println(s);
```

> caelum

* isso acontece pq o método não altera a string original, mas retorna um novo objeto
* dessa forma, a nova string deve ser associada a uma outra variável, ou mesmo sobrescrever a referencia da propria variavel

# charAt

* o método charAt devolve um char contido na string, com o índice informado
* se o índice for negativo ou maior do que o tamanho da string, java lança um StringIndexOutOfBoundsException

# criando e manipulando strings

* há duas maneiras de criar objetos do tipo string

```java
String nomeDireto = "Java";
String nomeIndireto = new String("Java");
```

* nao é possível criar uma string utilizando o construtor e fornecendo o parametro nulo
* 


* o construtor da classe string também pode receber um array de char, um stringbuilder ou um stringbuffer
* é possível concatenar um null e um literal do tipo string, sendo que nesse caso, o valor null será transformado em um literal
* não é possível concatenar o valor de uma string inicializada com uma string não inicilizadas
  * isso é diferente de concatenar com uma string iniciliazada como nula

* java faz casting implicitamente, respeitando a precedencia de operadores
* 

# Diferença entre concat e append

```java
    String s = "Caelum";
    s.concat(" - Ensino e Inovação");
    System.out.println(s);
```

> Caelum

```java

    StringBuffer s = new StringBuffer("Caelum");
    s.append(" - Ensino e Inovação");
    System.out.println(s);
```

> Caelum  - Ensino e Inovação
    
```java
class A {
    public static void main(String[] args) {
        int valor = 10;
        int dividePor = 4;
        double resultado = valor / dividePor;
        System.out.println(valor + dividePor + "");
        System.out.println("" + resultado + valor );
    }
}

```

> 14
>
> 2.010

# replace

* exige dois chars ou duas strings

# indexOf e lastIndexOf

* indexOf retorna o índice. Se nao for encontrado, retorna -1

```
String texto = "Pretendo fazer a prova de certificação de Java";
System.out.println(texto.indexOf("tendo")); // imprime 3
```
* no exemplo acima, se houver _match_, o método retorno a posição do primeiro caractere

# contains, startsWith e endsWith

```java
System.out.println(texto.startsWith("Pretendo")); // true
System.out.println(texto.startsWith("Pretendia")); // false

System.out.println(texto.endsWith("Java")); // true
System.out.println(texto.endsWith("Oracle")); // false

System.out.println(texto.contains("Pretendo")); // true
System.out.println(texto.contains("Pretendia")); // false

```

* os métodos contains, startswith e endswith são booleanos, ou seja, não retornam posições
* nenhum desses métodos trabalha com expressoes regulares

# equals e compareTo

* enquanto os métodos startswith, endswith e contains verificam se uma string está contida em outra, ou seja uma string começa/termina com outra, os métodos equals e compareTo verifica se o _match_ é exato
* equals é booleano, compareTo retorna um valor numérico
* compareTo retorna zero se houver match e outras valores, caso contrário
* ambos os métodos aceitam a variação ignoreCase

# outros métodos de string

* length() retorna a quantidade de caracteres (inclusive espaços em branco)
* isEmpty() retorna verdadeiro se a string tiver zero caracteres (considera caracteres em branco)
* toUpperCase() e toLowerCase() tornam a string toda maiúscula ou minúscula, respectivamente
* substring(inicio, fim) retorna um novo objeto string contendo os caracteres no intervalo \[inicio,fim\[ da primeira string
* concat() concatena strings
* replace( oldChar, newChar) substitui todas as ocorrencias do antigo caractere pelo novo
* replace (target, replacement) substitui todas as ocorrencias de uma sequencia de caracteres por outra
* trim() remove os espaços em branco das duas pontas 

# substring

* o método substring tem duas sobrecargas: uma que aceita dois índices (começo e fim); e outra que aceita apenas o início da substring, percorrendo-a até o final
* se o início for maior do que o tamanho; se o inicio for maior do que o fim; se o fim for maior do que o tamanho; se o início for menor do que zero; ou se o início for maior do que o fim, o método lançará uma exceção
* 
