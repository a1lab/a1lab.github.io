# Operadores

* O símbolo de igual é responsável por fazer uma atribuição

## Aritmeticos
* + soma
* - subtração
* * multiplicação
* / divisao
* % resto

Pode-se utilizar o igual e os operadores artimeticos para fazer uma atribuição composta

x += 2; // x = x + 2;

O operador de soma, quando utilizado com strings concatena-as

## Operadores unários

O símbolo de negativo torna negativo o valor numérico de uma expressão
O símbolo de exclamação inverte o valor de um tipo booleano
O símbolo de ++ incremente em 1 o valor
-- Decrementa em 1
Esse operador pode ser prefixado ou pósfixado
*Exemplo de uso prefixado e pósfixado

## Igualdade e relações

==      equal to
!=      not equal to
>       greater than
>=      greater than or equal to
<       less than
<=      less than or equal to

## Operadores condicionais

Os operadores condicionais em Java são do tipo short-circuiting, ou seja, se a condição mais a esquerda falhar, as demais condições não serão avaliadas

&& Conditional-AND
|| Conditional-OR

Outro operador condicional é o ?: (if ternário)

The instanceof operator compares an object to a specified type. You can use it to test if an object is an instance of a class, an instance of a subclass, or an instance of a class that implements a particular interface.

Se uma classe é filha de outra, o operador instanceof, quando aplicado à classe-mãe, retornará verdadeiro

Exemplo: class Parent{}, class Child extends Parent{} implements Family
child instanceof Child //true
child instanceof Parent //true
child instanceof Family //true

