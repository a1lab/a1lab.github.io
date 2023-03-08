# Classe Character

* assim como nos casos de tipos primitivos numéricos, java também prove um wrapper para o tipo char
* da mesma forma, java também provê unboxing e autoboxing
* um Wrapper é imutavel, ou seja, uma vez criado, não pode ter seu valor alterado

* a classe Character possui métodos estáticos muito relevantes
* isLetter verifica se o caractere é uma letra; idDigit, se é um número
* também há os métodos isWhitespace isUpperCase, isLowerCase; além de toUpperCase, toLowerCase e toString



* Número normalmente são declarados como tipos primitivos

```
	int i = 500;
	float gpa = 3.65f;
	byte mask = 0x7f;
```

* Contudo, existem motivos para utilizar objetos ao invés de tipos primitivos. Java provê classes nativas para isso: os wrappers
* Eventualmente o encapsulamento é feito pelo compilador, se vc usar um tipo primitivo em um trecho de código no qual um objeto é esperado
** Esse processo é chamado de autoboxing e unboxing
* Todos os wrappers herdam de Number: Byte, Integer, Double, Short, Float, Long
* Além dos wrappers, existem outras 4 classes que herdam de Number: BigDecimal, BigInteger, AtomicInteger e AtomicLont
** As duas primeiras servem para fazer calculos com maior precisão; as duas útlimas, para manipular numeros em sistemas multi-thread
* Razões para usar um objeto ao invés de um tipo primitivo
** Para facilitar a manipulação de coleções, visto que não há como instanciar coleções de tipos primitivos
** Para usar constantes, como MIN_VALUE e MAX_VALUE
** Para usar métodos de classe (estáticos) para converter valores de um tipo primitivo para outro, como entre um tipo numérico e uma string, ou para converter entre sistemas numéricos 

* Toda subclasse de Number implementa métodos que convertem a instância de Number em uma instância de um wrapper de outro tipo primitivo, facilitando a conversão de tipos para byte, short, int, long, float e double
* Além disso, também implementam os métodos compareTo, para cada tipo de dado primitivo; e o método equals
** se o valor da instancia que invocou o método compareTo for menor do que o argumento do método, o retorno é -1; se for maior, 1; se for igual, 0.
** O método equals retorna verdadeiro se o valor for igual; falso se for diferente, sem determinar se o valor é maior ou menor

*As subclasses de Number implementam também métodos para converter de/para tipos numéricos e strings
** decode converte uma representação decimal, octal, hexadecimal para um numero
** parseInt converte uma string decimal para um inteiro
** parseInt(String s, int radix) converte também de acordo com o tipo numerico radix
** toString retorna o valor em uma stgring
** valueOf converte de um tipo primitivo para o wrapper
** valueOf converte de uma string para um wrapper

# Formatação de valores numéricos

* Existem métodos que podem ser usados para imprimir texto formatado, como System.out.format
* O primeiro argumetnodo método é o texto com especificadores de formatação
* O segundo argumento é um varargs, cujo tamanho deve coincidir com a quantidade de especificadores de formatação


```
System.out.format("The value of " + "the float variable is " +
     "%f, while the value of the " + "integer variable is %d, " +
     "and the string is %s", floatVar, intVar, stringVar); 
```  
     
* São exemplos de formatadores https://docs.oracle.com/javase/tutorial/java/data/numberformat.html
Converter	Flag	Explanation
d	 	A decimal integer.
f	 	A float.
n	 	A new line character appropriate to the platform running the application. You should always use %n, rather than \n.
tB	 	A date & time conversion—locale-specific full name of month.
td, te	 	A date & time conversion—2-digit day of month. td has leading zeroes as needed, te does not.
ty, tY	 	A date & time conversion—ty = 2-digit year, tY = 4-digit year.
tl	 	A date & time conversion—hour in 12-hour clock.
tM	 	A date & time conversion—minutes in 2 digits, with leading zeroes as necessary.
tp	 	A date & time conversion—locale-specific am/pm (lower case).
tm	 	A date & time conversion—months in 2 digits, with leading zeroes as necessary.
tD	 	A date & time conversion—date as %tm%td%ty
 	08	Eight characters in width, with leading zeroes as necessary.
 	+	Includes sign, whether positive or negative.
 	,	Includes locale-specific grouping characters.
 	-	Left-justified..
 	.3	Three places after decimal point.
 	10.3	Ten characters in width, right justified, with three places after decimal point.
 	
 	
```

# a classe DecimalFormat
* a classe java.text.DecimalFormat pode ser usada para controlar a impressao de zeros à esquerda, prefixos, sufixos, pontos de casa decimal, etc.
* o método de instancia format recebe um valor qualquer; ao passo que a criação da instância exige um padrão
* o resultado do método é a string formatada com o padrão
* o símbolo # denota um dígito, podendo incluir pontos e vírgulas entre os dígitos
* também é possível adicionar sufixos ou prefixos
* por fim, é possível utilizar zeros no lugar de ### para definir um padrão

```
DecimalFormat myFormatter = new DecimalFormat(pattern);
      String output = myFormatter.format(value);
123456.789  ###,###.###  123,456.789
123456.789  ###.##  123456.79
123.78  000000.000  000123.780
12345.67  $###,###.###  $12,345.67
```

# além dos números
* a classe java.lang.Math provê métodos para fazer aritmética mais arrojada do que os operadores +,-,*,/ e %
* além das constantes E e PI, todos as funcoes trigonométricas são contempladas sin, cos, tan, asin, a cos, atan, toDegres, toRadians...
* o método ceil retorno o menor valor inteiro maior do que o argumento decimal; floor, o maior valor inteiro menor do que o argumento
* rint retorna o valor inteiro mais próximo do valor decimal
* round arredonda o valor
* min retorna o menor de dois valores; max, o maior
* abs retorna o valor absoluto (remove o sinal de negativo, se houver)

```
	ceil(43.51) = 44
	flor(43.51) = 43
	rint(43.51) = 44
	rint(43.49) = 43
```

# valores exponenciais e logaritmos
* exp retorna e^argumento
* log retorna o logaritmo natural do argumetno dado
* pow eleva o primeiro argumento ao segundo
* sqrt retorna a raiz quadrada do argumento

* a raiz n-ésima de um número pode ser calculada como o número elevado a 1/n
* dessa forma, é possível utilizar a funcao pow para calcular
* double root(double x , int n){ return Math.pow(x , (1/n)));

# numeros aleatórios
* para criar numeros aleatórios, basta usar uma instancia da classe Random

```
	Random r = new Random();
	r.nextInt(200);//cria um int de 0 a 200
```

```java
package fundamentos.numeros;

public class Numeros {

	public static void main(String[] args) {
		Integer valor = 10;
		System.out.println(valor.byteValue());
		System.out.println(valor.shortValue());
		System.out.println(valor.intValue());
		System.out.println(valor.longValue());
		System.out.println(valor.floatValue());
		System.out.println(valor.doubleValue());

		System.out.println(valor.compareTo(11));
		System.out.println(valor.compareTo(10));
		System.out.println(valor.compareTo(9));
	
		Integer binarioEmInteiro = Integer.decode("0101");
		System.out.println(binarioEmInteiro);
		
		System.out.println("raiz cúbica de 8 é = " + root(8,3));
	}

	public static double root(double x , double n) {
		return Math.pow(x, (1/n));
	}
	
}

```


