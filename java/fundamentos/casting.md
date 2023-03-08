
# Casting

* _Casting_ é uma operação em que o valor de um literal é truncado para outro tipo de dado.
* No exemplo abaixo, a variável **valorInteiro** é incapaz de guardar um valor decimal. Por isso, o valor do literal decimal associado a ela é truncado para um valor diferente do original, de modo que ele possa ser representado em outro tipo de dado.

```java
  int preco = 10.50
```

> A variável **preco** assume o valor inteiro **10**, ao invés de **10.50**.

* Se um literal de um tipo for associado a uma variável de outro tipo, de modo que o tamanho do tipo do literal seja menor do que o do tipo da variável, Java converte o tipo do literal para o tipo da variável, sem perda de informação.
* No exemplo abaixo, o literal **1** é do tipo **int**, mas a variável **valor** é do tipo **long**. Nesse caso, como o valor do literal é menor do que o tamanho da variável, Java converte o tipo do literal implicitamente.

```java
  long valor = 1;
```

* Se um literal for associado a uma variável, de modo que o valor do literal for maior do que o tamanho permitido pelo tipo da variável, Java converte o tipo do literal, sem garantir -contudo- que não haverá perda de informação.
* No exemplo abaixo, o literal **128** é do tipo **int**, e é maior do que o limite permitido pelo tipo **byte** da variável **valorEmByte**.
* O tipo primitivo **byte** aceita apenas valores entre **[^-2^8 , 2^8 - 1]**, ou seja, entre **[-128 , 127]**. Como o valor do literal é maior do que o limite superior, o compilador vai apontar o seguinte erro:

```java
  byte valorEmByte = 128;
```

> Type mismatch: cannot convert from int to byte

* Para resolver esse problema, é necessário converter explicitamente o tipo do literal. Dessa forma, o programador declara que tomou ciência sobre a conversão forçada e as eventuais inconsistências.

```java
  byte valorEmByte = (byte) 128;
``` 

> DE/PARA	byte	short	char	int	long	float	double
> byte	----	Impl.	(char)	Impl.	Impl.	Impl.	Impl.
			short	(byte)	----	(char)	Impl.	Impl.	Impl.	Impl.
			char	(byte)	(short)	----	Impl.	Impl.	Impl.	Impl.
			int	(byte)	(short)	(char)	----	Impl.	Impl.	Impl.
			long	(byte)	(short)	(char)	(int)	----	Impl.	Impl.
			float	(byte)	(short)	(char)	(int)	(long)	----	Impl.
			double	(byte)	(short)	(char)	(int)	(long)	(float)	----
