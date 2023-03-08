
## Escopo de variáveis locais

* O escopo das variáveis locais está limitado ao bloco mais restritivo. Variáveis declaradas dentro de condicionais e laços só podem ser acessadas nos corpos de tais condicionais e laços. Os dois exemplos abaixo ajudam a ilustrar a situação
* No primeiro exemplo, como a variável local **desconto** foi declarada dentro do corpo do primeiro condicional, ela não pode ser acessada fora dele, causando um erro de compilação, como se a variável não tivesse sido declarada antes.

```java
  int quantidadeDePessoas = 3;
  if(quantidadeDePessoas > 1){
  	boolean desconto = true;
  } else{
  	if(desconto){
	   ...
	}
  }
```

* Neste segundo exemplo, o compilador também lançará um erro, pois a variável **valorDoDesconto** foi declarada dentro do condicional mais aninhado, portanto não pode ser acessada fora dele. A variável deixa de existir na memória da aplicação ao término da execução daquele bloco. Perceba que neste segundo exemplo, a variável **desconto** foi declarada no condicional mais externo e por isso pode ser acessada pelo condicional mais aninhado, sem causar o mesmo erro que o exemplo anterior.

```java
  double valorCheio = 100;
  int quantidadeDePessoas = 3;
  if(quantidadeDePessoas > 1){
    boolean desconto = true;
    if(desconto){
    	double valorDoDesconto = 10.89;
	...
    }
    double valorFinal = valorCheio - valorDoDesconto;
  } 
  }
```
