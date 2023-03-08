
# Operadores _bitwise_ e _bit shift_

* Java fornece operadores que permitem realizar operações do tipo _bitwise_ e _bitshift_ sobre tipos inteiros.
* São dois os propósito desta aula extra: apresentar tais operadores; e diferenciá-los dos operadores lógicos.
* Nos dois exemplos abaixo, são efetuadas operações _bitwise_ dos tipos **OR** e **AND**, respectivamente. Perceba que apesar dos símbolos serem idênticos aos dos operadores lógicos **OR** e **AND**, eles produzem resultados completamente diferentes. No caso dos operadores lógicos, o resultado é uma expressão booleana, que pode ser verdadeira, ou false; no caso dos operadores _bitwise_, o resultado é um valor inteiro, cuja representação binária foi modificada pela operação realizada.



# Left shift

```java
  byte a =      0b0000_1100;
  a = a << 2; //0b0011_0000;
```

# Right shift signed

```java
  byte a =      0b0000_1100;
  a = a >> 2; //0b0000_0011;
```

* 

```java

```

	static void rightShiftSignedNegativeNumber() {
		System.out.println(-0b00001000);		//1000 = 8
												//0111		complemento de 1
												//1000		complemento de 2
												//1110 = -2	right shift
		System.out.println(-0b00001000 >> 2);	//0010 = 2  // right shift de 2 bits. Como 8 é positivo, os bits a esquerda são preenchidos com zeros		
	}

	static void rightShiftUnsigned() {
		/*
		 * 8 			00001000
		 * 8 >>> 2 		00000010
		 * -8			00001000
		 * -8 >>> 2		00000010		//1073741822
		 */
		
		int number1 = 8;					//00001000
		    int number2 = -8;					
		    
		    // 2 bit signed right shift
		    System.out.println(number1 >>> 2);    // prints 2
		    System.out.println(number2 >>> 2);    // prints 1073741822	}
	}
	
}
