# IF

* um  if testa uma condiçao booleana

```
int a = 0, b = 1;
if(a = b) {
    System.out.println("iguais");
} 
```
> Não compila, pois a expressão não é booleana, mas de atribuição

```java

boolean a = true;

if(a = false) {
    System.out.println("Falso!");
} 
```

> compila, pois apesar de ser uma instrução de atribuição, o resultado é booleano

* o bloco de instruções do IF, embora tenha chaves opcionais, é obrigatório. Pelo menos uma instrução deve haver no bloco if

# unreachable code e missing retunr

* um código java não compila se houver uma instrução após uma instrução de retorno, ou se um if nunca for verdadeiro
* 

# switch

um switch aceita um int, um wrapper ou qualquer tipo inteiro menor que um int
ou seja, não é possível fazer switch com long
switch tambem aceita strings e enunms
o tipo dos cases deve ser compatível com o tipo da expressao condicional
atenção: switch só aceita tipos inteiros

um switch aceita constantes, desde que sejam declaradas e inicializadas na mesma linha
nao é possível usar variáveis no lugar dos cases

o default não precisa vir por ultimo, alias, pode vir por primeiro ou no meio dos cases

cases podem nao ter nenhum bloco de codigo no meio, o que equivale a concatenar OR entre os casos

switch só aceita comparações de igualdade, nao aceita desigualdade, nem relacoes

