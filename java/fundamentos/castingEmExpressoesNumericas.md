

      
## Casting em expressões aritméticas

```java

		System.out.println(3.14/2);
		System.out.println(5/2);//valor esperado era 2.5, mas java vai atribuir 2
		System.out.println((double) 5/2);
		System.out.println(5/(double)2);
		System.out.println((double) (5/2)); //aqui primeiro será feita a divisão, depois a atribuição em um inteiro
		System.out.println(5.0/2);//ao declarar com ponto, java vai interpretar como um double
		System.out.println(5/2.0);//ao declarar com ponto, java vai interpretar como um double

		//casting
		double salario = 1270.50;
		int salarioInteiro = (int) salario;
		System.out.println("salario convertido em inteiro " + salarioInteiro);
```
