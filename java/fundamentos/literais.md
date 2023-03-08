
# Literais

Os literais são elementos da linguagem de programação que representam valores particulares. Java possui 5 tipos de literais:

* **Booleanos**. _true_ ou _false_.
* **Inteiros**. Exemplos: 100, 7, 365, etc.
* **Decimais**. Exemplos: 10.50, 3.14, 1.99, etc.
* **Caracteres**. 'a', 'B', 'c', 'Z', etc.
* **Cadeias de caracteres**. "Nome", "Bairro", "Valor", etc.

Os literais podem ser utilizados nas senteças de inicialização de variáveis e como argumentos de métodos, tanto de forma independente ou empregados em expressões. No exempo abaixo, na primeira sentença, os literais decimal e inteiro (respectivamente) **17.32** e **2** são empregados em uma expressão aritmética; na segunda sentença, o literal inteiro **19** é utilizado na inicialização da variável **idade**; na terceira sentença, a variável **idade** e o literal inteiro **18** são aplicados em uma expressão booleana, cujo resultado é associado à variável **maiorDeIdade**; e por fim, na última sentença, os literais **Valor da compra = R$** e **10.50** são fornecidos como argumentos ao método estático **println** da classe **System.out**.

```java
  double valor = 17.32 * 2;
  int idade = 19;
  boolean maiorDeIdade = (idade >= 18); //true
  System.out.println("Valor da compra = R$" + 10.50);
  ```

## Literais de caracteres simples e cadeias de caracteres

* Literais de caracteres simples devem ser declarados com aspas simples.
* Também é possível associar um valor numérico a uma variável de tipo **char**

```java
  char c= 1;
```

* The Java programming language also supports a few special escape sequences for char and String literals: \b (backspace), \t (tab), \n (line feed), \f (form feed), \r (carriage return), \" (double quote), \' (single quote), and \\ (backslash).

* Literais de cadeias de caracteres devem ser declarados com aspas duplas.

```java
public class CaracteresEstrings {

	public static void main(String[] args) {
		char letra = 'a';//char guarda uma única letra e o literal deve ser declarado com aspas simples
		//o char guarda um valor de 16bits, que é convertido usando uma tabela unicode,
		//que é maior do que a tabela ascii, não tem um limite definido e guarda ideogramas, emojis, etc
		
		char a = 65;
		
		char b = 66;
		char c = (char) (b + 1);
		System.out.println(a + b + c);//vai imprimir 198 = 65 + 66 + 67
		System.out.println(c);//vai imprimir c
		
		String palavra = "palavra";//um string guarda vários caracteres e é uma instancia da classe string do java
		System.out.println(palavra + palavra);//as variáveis são concatenadas
		
		
		
	}
	
}


```
* sequencias escapadas
* se um caracter é precedido de uma barra invertido, trata-se de uma sequencia escapada e isso tem um significado especial para o compilador
* \t insere uma tabulação
* \b insere um backspace
* \n quebra a linha
* \r um ponto de retorno
* \f
* \' insere uma aspas simples
* \" aspas duplas
* \\ barra invertida

```

She said "Hello!" to me.
you would write

System.out.println("She said \"Hello!\" to me.");
```

## Literais especiais

* null pode ser associado a qualquer tipo de referência
* * Um tipo especial de literal String é o literal que representa o nome de uma classe. 

# Exercícios

1. Dado que o campo estático **Integer.MAX_VALUE** representa o maior valor que pode ser armazenado em um **int**, qual é o valor impresso no console pela sentença abaixo? (Neste exercício, o _wrapper_ **Integer** e o tipo primitivo **int** podem ser considerados como equivalentes.)

```java
  System.out.println(Integer.MAX_VALUE + 1);
```

# Não compilado


* a palavra reservado 'final' pode ser usada para dizer ao compilador que o valor de determinada variável é constante e nunca será alterada
* Em geral, ao falar de campos, trata-se dos campos de uma classe, estáticos ou de instância
* Variáveis podem ser entendidas tanto como variáveis locais, parâmetros ou campos 
* Os campos, métodos e tipos aninhados são chamados de membros da classe


* valores de variaveis do tipo byte, short, int e long podem ser criadas com literais int
* valores do tipo long podem ser criados com literais long
* se o valor de um literal for maior do que o tipo da variável, é necessário fazer um cast, com eventual perda de informação/inconsistência
