# Call stack

* No eclipse é possível executar a aplicação linha por linha, clicando na opção step-over
* Ao executar uma linha de código, tudo o que está contido dentro dela será executado

```java
public class Fluxo {

	public static void main(String[] args) {
		System.out.println("inicio do main"); // break point
		metodo1();
		System.out.println("fim do main");
	}

	public static void metodo1() {
		System.out.println("inicio do metodo1");
		metodo2();
		System.out.println("fim do metodo1");
	}

	public static void metodo2() {
		System.out.println("inicio do metodo2");
		for (int i = 1; i <= 5; i++) {
			System.out.println(i);
		}
		System.out.println("fim do metodo2");
	}

}

```

* No exemplo acima, antes do _break point_, a saído do console será:

> inicio do main

* Ainda no exemplo acima, ao executar um _step over_, todas as instruções do **metodo1()** serão executadas, incluindo suas chamadas internas ao **metodo2()**.
* A saída do console será

> inicio do main
> 
> inicio do metodo1
>
> inicio do metodo2
> 
> 1
>
>  2
> 
> 3
> 
> 4
> 
> 5
> 
> fim do metodo2
> 
> fim do metodo1

* Para acompanhar a execução instrução por instrução, é necessário utilizar o _step into_
* Na _view Debug_ é possível acompanhar a criação da pilha de execução e as chamadas dos métodos sendo empilhadas.

# Motivações

* Motivações para sinalizar que um método não funcionou adequadamente:
  * um método void poderia ser alterado para retornar boolean, informando que o fluxo foi normal. Mas se quem o chamou não consumir o seu retorno, não faz diferença
  * um método que retorna um valor numérico poderia retornar -1. Mas se o domínio do retorno for também negativo, convencionar o valor -1 pode causar confusao
  * um método que retorna um tipo, poderia retornar Object, mas quem consome o resultado precisaria fazer um cast desnecessário, e também seria sempre necessario fazer um instanceof, para verificar se o tipo de retorno não é um tipo de erro
  
 # Tratamento de exceções
 
 ```java
public class Fluxo {

	public static void main(String[] args) {
		System.out.println("inicio do main");
		metodo1();
		System.out.println("fim do main");
	}

	public static void metodo1() {
		System.out.println("inicio do metodo1");
		try {
			metodo2();
		} catch (ArithmeticException e) {
			System.out.println(e.getClass().getCanonicalName());
		}
		System.out.println("fim do metodo1");
	}

	public static void metodo2() {
		System.out.println("inicio do metodo2");
		for (int i = 1; i <= 5; i++) {
			System.out.println(i);
			int a = i / 0;
		}
		System.out.println("fim do metodo2");
	}
```

# Call stack e o tratamento de exceções

```java
public class Fluxo {

	public static void main(String[] args) {
		System.out.println("inicio do main");
		try {
			metodo1();
		} catch (NullPointerException e) {
			System.out.println("NullPointerException");
		}
		System.out.println("fim do main");
	}

	public static void metodo1() {
		System.out.println("inicio do metodo1");
		try {
			metodo2();
		} catch (ArithmeticException e) {
			System.out.println(e.getClass().getCanonicalName());
		}
		System.out.println("fim do metodo1");
	}

	public static void metodo2() {
		System.out.println("inicio do metodo2");
		for (int i = 1; i <= 5; i++) {
			System.out.println(i);
			// int a = i / 0;
			Fluxo fluxo = null;
			fluxo.metodo();
		}
		System.out.println("fim do metodo2");
	}
  
	public void metodo(){}
}
```

# Catch múltiplo

```java
try {
  metodo1();
} catch (ArithmeticException | NullPointerException e) {
  System.out.println("Ocorreu uma exceção.");
}
```

