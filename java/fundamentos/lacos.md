# Laços

* laços serve para alterar o fluxo de exceução de um programa, instruindo o sistema a exceutar uma instrução repetidas vezes
* assim como nos condicionais, um laço exige a verificação de uma condição booleana
  * enquanto ela for verdadeira, o corpo do laço será executado

* se houver uma isntrução após um laço infinito, o programa não compila

```java
while(true){
  System.out.println("");
}
System.out.println("");//nunca será executado
//
```

> unreachable statement

* se em tempo de compilação, a análise sintática não puder determinar que se trata de um laço infinito, o programa compila normalmente

```java
int valor = 0;
while (valor != 5){
  System.out.println("");
}
System.out.println("");//nunca será executado
```

> Compila, mas gera uma laço infinito

* se um laço nunca for executado, isso também causa um erro de compilaçai

```java
while(5> 10){
  System.out.println("");
}
```

> unreachable statement

```java

int a = 1;
int b = 2;
while(a > b){ //compila, mas nunca executa
    System.out.println("OI");
}
```

> compila, mas não executa apropriadamente

# tipos de lacos

* o for é preferível qunado sabemos a quantidade de iterações
* o enhanced-for é preferível qunado for uma iteração de leitura
  * nao é possível percorrer mais de uma coleção ao mesmo tempo
  * nao é possível remover ou alterar a coleção original
  * nao é possível inicializar um array com esse tipo de laço


