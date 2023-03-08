# Representação binária de um decimal

* Todo número inteiro pode ser representado como a soma de uma sequência de potências de base 2, em que o expoente é incrementado de 1 em 1, começando em 0.

> 75 = 64 + 8 + 2 + 1
> 
> 75 = 2^6 + 2^3 + 2^1 + 2^0

* Como os termos **2^2**, **2^4** e **2^5** estão ausentes, podemos representá-los, multiplicando-os pelo fator 0. Desse modo, o resultado não será alterado.

> 75 = 1\*2^6 + **0\*2^5** + **0\*2^4** + 1\*2^3 + **0\*2^2** + 1\*2^1 + 1\*2^0

* Veja outros exemplos:

> 5 = 4 + 1 = 1\*2^2 + 0\*2^1 + 1\*2^2
>
> 32 = 32 = 1\*2^5 + 0\*2^4 + 0\*2^3 + 0\*2^2 + 0\*2^1 + 0\*2^0 

* Desde que toda potência seja representada de forma ordenada em função de seu expoente, do maior para o menor, mesmo que seus fatores sejam 0, podemos omiti-las, mantendo apenas os fatores. Cada uma dessas potências vamos chamar de bit.

> 75 = 1001011
> 
> 5 = 101
>
> 32 = 10000

* Por convenção, vamos representar os valores com a mesma quantidade de bits.

> 75 = 1001011
> 
> 5 =  0000101
>
> 32 = 0010000

* Em Java, o tipo primitivo **byte** guarda 8 bits de informação, contudo o oitavo bit mais à esquerda é reservado para representar valores negativos; é o chamado **bit de sinal**.  
* Aqui há uma diferença na maneira como o valor é calculado: o bit de sinal, na verdade, equivale a **-2^8**, ou seja, **-128**.
* Por enquanto, perceba que o valor **-75**, por exemplo, não pode ser representado simplesmente adicionando o bit de sinal à sua representação binária **1001011**. O exemplo abaixo demonstra o que acontece se fizermos isso.

> 01001011 =  **-0\*2^7** + 1\*2^6 + 0\*2^5 + 0\*2^4 + 1\*2^3 + 0\*2^2 + 1\*2^1 + 1\*2^0 = +75
> 11001011 =  **-1\*2^7** + 1\*2^6 + 0\*2^5 + 0\*2^4 + 1\*2^3 + 0\*2^2 + 1\*2^1 + 1\*2^0 = -53

* Então, qual operação deve ser realizada para obter a representação binária de um valor negativo? 
* Antes de responder essa pergunta, vamos ver algumas operações que podem ser realizadas sobre valores binários: **OR, AND, NOT** e **XOR**.

# OR

```java
  byte a = 12; 		//0b0000_1100;
  byte b = 25; 		//0b0001_1001;
  byte c = a | b;	//0b0001_1101; 
```

# AND

```java
  byte a = 12; 		//0b0000_1100;
  byte b = 25; 		//0b0001_1001;
  byte c = a & b;	//0b0000_1000; 
```

# NOT

```java
  byte a = 0b0100_1011;
  a = ~a;//0b1011_0100;
```

# XOR

```java
  byte a = 12; 		//0b0000_1100;
  byte b = 25; 		//0b0001_1001;
  byte c = a ^ b;	//0b0001_0101; 
```


# Complemento de 2

* Agora que conhecemos a operação **NOT**, podemos definir o complemento de 2, que é a operação utilizada para obter a representação binária de um número negativo.
* O complemento de 2 é calculado como a negação do valor original, seguida da adição de 1 bit.

```java
  byte a = 0b0010_0101;   // 1 + 4 + 32 = 37 
  a = ~a;//0b1101_1010;   // 2 + 8 + 16 + 64 - 128 = -38
  a++;   //0b1101_1011;   // 1 + 2 + 8 + 16 + 64 - 128 = -37
```

* Perceba que a ordem das operações altera o resultado final. Se fizermos o contrário, somar 1 bit e depois calcularmos o complemento, o resultado será -39, ao invés de -37.

0010_0101 37
0010_0110 38
1101_1001 1 + 8 +16 + 64 -128
      
* Entender como Java representa valores inteiros por meio de representações binárias permite também compreender a perda de informação causada por um _type casting_.

```java
  byte a = 127;		//0b0111_1111 = 64 + 32 + 16 + 8 + 4 + 2 + 1 = 127
  a++; 			//0b1000_0000 = -128
```

* No exemplo acima, a variável **a** é inicializada com o maior valor possível para o tipo **byte**. Adicionar o valor **1** à essa variável, equivale a adicionar 1bit a ela. Dessa forma, ao adicionar um bit, todos os demais passam a valer **0**, e apenas o bit de sinal passa a ter valor **1**. Assim, o valor da variável **a** passa a ser **-128**.
