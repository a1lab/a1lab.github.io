 # Expressoes
 
Uma expressão é um constructo constituído por variáveis, operadores e invacações de métodos
Uma expressao sempre retorna um valor unico
o tipo do valor retornado depende dos tipos envolvidos na expressao
A avaliação de expressões tem precedencia, como na aritmetica. Se necessário, é possível usar parênteses balanceados

Statements

Uma sentenção é uma unidade de execução completa, como incrementos/decrementos, atribuições, invocação de métodos ou criação de objetos
Além disso, existem sentenças de declaração de variáveis e controle de fluxo

Blocos 

Blocos são um grupo de uma ou mais sentenças declaradas entre chaves balanceadas

Controle de fluxo

o statement if-then diz ao programa que as senteças contidas no bloco devem ser executadas somente se a condição for válida
o statement if-then-else diz ao programa que as senteças contidas no primeiro bloco devem ser executadas se a condiçao for verdadeiro, caso contrário as senteças do segundo bloco devem ser executadas
também pode-se utilizar um else sem if ao final, para dizer ao programa o q fazer caso nenhuma condição seja atendida

Switch

O switch nao funciona testando uma expressao booleana
Switch só funciona com byte, short, char, int Byte, Short, Integer e Character
Também é possível usar switch com Enum
A expressão do switch pode envolver mais de uma variável, envolvendo uma operação, desde que ela possa ser avaliada como um valor único
Exemplo switch(idade + trintaAnos)

A partir do Java 7 é possível usar switch com strings

Return statement

além de break e continue, outro branching statement é o retunr
return é usado para retornar o valor em um método
ou pra interromper a execuçao de um blocko
