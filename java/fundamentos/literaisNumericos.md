## Literais numéricos

Dois tipos de literais merecem especial atenção: os inteiros e decimais. Java utiliza tipos primitivos para representar esses valores, de modo que, dependendo de seu tamanho e precisão, pode ser necessário empregar tipos mais apropriados. 

Por padrão, o tipo primitivo utilizado em literais inteiros é o **_int_**, cujo tamanho é de **32bits**, ou seja, só consegue guardar valores entre **[-2^32, 2^32 - 1]**. Para utilizar literais com valores fora dessa faixa, é necessário informar ao compilador de que se trata de um tipo **_long_**. Isso pode ser feito adicionando os caracteres **l** ou **L** logo após o valor do literal. Embora o efeito seja o mesmo, o uso do caractere minúsculo **l** é desencorajado, por dificultar a leitura e causar confusão com o número **1**. 

Por outro lado, se o valor estiver contido no intervalo acima mencionado, não é necessário adicionar nenhum caractere para informar ao Java de que se trata de um número inteiro.  

Por padrão, o tipo primitivo utilizado em literais decimais é o **_double_**, com precisão dupla e tamanho igual a **64bits**, ou seja, consegue guardar valores entre **[-2^64, 2^64 - 1]**. Se o valor do literal estiver contido no intervalo **[-2^32, 2^32 - 1]**, e a precisão dupla for desnecessária, pode-se utilizar o tipo primitivo **_float_** em seu lugar. Isso pode ser feito adicionando os caracteres **f** ou **F** logo após o valor do literal. Embora o efeito seja o mesmo, o uso do caractere maiúsculo **F** é convencional.

Ainda que seja permitido declarar um literal decimal do tipo **_double_** com os caracteres **d** ou **D** ao final do valor, isso é opcional. 

Em suma, todo literal numérico inteiro é do tipo **int**; decimal, do tipo **double**. Se for necessário utilizar os tipos **long** ou **float**, é necessário adicionar os caracteres **L** ou **F** -respectivamente- logo após o valor do literal.
