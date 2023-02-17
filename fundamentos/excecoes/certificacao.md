* todo exceção em sentido amplo herda de throwable
* errors são reservados para os desenvolvedores da jvm. Trata-se de exceções que causam falhas irreparáveis
* exceptions sao exceções das quais a aplicação pode se recuperar
* excpetions se dividem entre checked e unchecked
* exceç~es checked herdam diretamente de exception e são recuperáveis e previsíveis
* exceções unchecked não são previsíveis e por isso podem ser ignoradas em tempo de compilação
* exceções unchecked são filhas de RuntimeException
* isso tem um impacto na compilação do código

```java
public static void main(String[] args){
  String nome = null;
  nome.toLowerCase();
}
```

> java.lang.NullPointerException: Cannot invoke "String.toLowerCase()" because "nome" is null


```java
public static void main(String[] args){
   try {
			String nome = null;
			nome.toLowerCase();			
		} catch(RuntimeException e) {
			System.out.println(e);
		}
}
```

* O exemplo abaixo não compila, pois IOException é uma exceção _checked_ e o compilador verifica se a pilha de chamadas contida no bloco _try_ possui algum método que pode lançar uma exceção do tipo IOException.

```java
public static void main(String[] args){
   try {
			String nome = null;
			nome.toLowerCase();			
		} catch(IOException e) {
			System.out.println(e);
		}
}
```

* O Exemplo abaixo compila, pois NullPointerException é do tipo _unchecked_
```java
public static void main(String[] args) {
		try {
					
		} catch(NullPointerException e) {
			System.out.println(e);
		}
	}
```

* Se a exceção lançada no bloco try encontra um tratamento em um dos blocos _catch_, ele é tratada por esse bloco. Do contrário o fluxo simplesmente vaza e continua

# métodos que chamam outros métodos e a pilha de chamadas

* se o códgio tiver uma exceção checked, ele precisa necessariamente captura-la ou trta-la em tempo de compilacao, senao nao compila
* o método main nao pode jogar uma exceção
* se a exceção for lançada e o método main não tratá-la, ela vaza e o programa termina

* se houver código não alcançável abaixo de uma instrução **throw**, o códgio nça compila

# exceções tradicionais

```java
  int[] x = new int[2];
  x[2] = 1;
```

> ArrayIndexOutOfBoundsException

```java
  List<Integer> listaNumeros = new ArrayList<>();
  listaNumeros.get(0);
```

> IndexOutOfBoundsException

* Um **NullPointerException** ocorre ao tentar acessar um dos membros de um objeto não inicializado.
* Perceba que isso é diferente de não inicializar uma variável local. Nesse caso, o código sequer compila.

```java
  String nome = null;
  nome.length();
```

> NullPointerException

```java
  String nome = "João";
  Integer valor = (Integer) nome;
```

> ClassCastException

```java
  String numero = "numero";
  int valorDoNumero = Integer.parseInt(numero);
```

> NumberFormatException

```java
  public void depositar(double valor){
    if(valor < 0){
      throw new IllgalArgumetnException();
    }
    //demais instruções omitidas
  }
```

> IllegalArgumentException

```java
  private boolean contaInativa = true;
  private double saldo = 100.00;
  public void sacar(double valor){
    if(contaInativa){
      throw new IllegalStateException();
    }
  }
```  

> IllegalStateException

```
  class Pessoa{
    static {
      String nome = null;
      nome.length();
    }
  }
```

> NullPointerException
> 
> ExceptionInictializerError

```java
  public void metodo(){
    metodo();
  }
```

> StackOverflowError

* Se uma das bibliotecas não está no _classpath_

> NoClassDefFoundError

```java
  List<Integer> lista = new ArrayList<>();
  while(true){
    lista.add(1);
  }
```

> OutOfMemoryError
