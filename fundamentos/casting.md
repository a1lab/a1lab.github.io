# casting

* A atribuição de valores exige que o tipo da variável seja o mesmo tipo do valor literal atribuído. 
* Caso contrário, o tipo da variável deve ter o _range_ maior do que o tipo do literal
* Nesse caso, Java faz uma **autopromoção** do tipo do literal para um tipo maior

> byte (1) -> short (2) -> int -> long -> float -> double
> 
> char -> int

* No sentido contrário, Java é incapaz de fazer a **autopromoção**, de modo que é necessário indicar ao compilador o tipo para o qual o valor literal deve ser truncado.

```java
int x = 3/2;
System.out.println(x);
System.out.println((float) 3/2);
System.out.println((float) (3/2));
```

> 1
> 1.5
> 1.0

* No primeiro caso, o resultado da divisão de dois literais inteiros é um inteiro, com perda de informação. 
* No segundo caso, o _casting_ explícito é aplicado primeiro ao valor literal **3**. O resultado da operação assume o tipo do maior literal, que agora é o **float**.
  * Em outras palavras, Java está fazendo a operação 3.0 / 2.0, que resulta em 1.5
* No último caso, Java realiza primeiro a divisão entre inteiros, como no primeiro caso, resultando em um valor inteiro com perda de informação (1).
  * Em seguida, Java trunca esse valor para o tipo _float_, resultando em 1.0



