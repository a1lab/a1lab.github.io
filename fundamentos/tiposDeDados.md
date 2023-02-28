# Tipos de dados

* se o programa fizer uso de uma variável não inicilizada, o compilador não compila
  * isso pode acontecer se a variável for executada em um branch alternativa
  
* atenção: não é possível atribuir um valor inteiro para um boolean

# declaracao de variaveis

* toda variável local deve ser inicializada
* ela pode ser inicializada em uma linha e declarada em otura, mas deve ser inciializada antes de ser usada
* toda variável pode ser declarada e inicializada na mesma linha
* a declaracao de uma variavel instrui a maquina virtual a reservar um espaço na memória (heap) to tamnaho do tipo da variável, atribuindo-lhe um endereço
* o acesso ao endereço no nível de máquina é feito pela JVM; no nível da aplicação, através do nome da variável
* toda variável membro de uma classe (estática ou de instância) é inicializada com seu valor default
* na declaração de arrays tambem ocorre inciializacao implicita, utilizando o tipo default da variavel
* 

# notações

* numeros que começam com 0 são octais
* numeros que começam com 0x são hexa
* numeros que começam com 0b sao binarios

# tamanhos

Não há a necessidade de decorar o intervalo e tamanho de todos os tipos de primitivos para a prova. O único intervalo cobrado é o do byte (-128 a 127).

É importante também saber que o char, apesar de ter o mesmo tamanho de um short, não consegue armazenar todos os números que cabem em um short, já que o char só armazena números positivos.

# palavras reservadas

* sao 50 palavras-chave

abstract
assert
boolean
break
byte
case
catch
char
class
const
continue
default
do
double
else
enum
extends
false
final
finally
float
for
goto
if
implements
import
instanceof
int
interface
long
native
new
null
package
private
protected
public
return
short
static
strictfp
super
switch
synchronized
this
throw
throws
transient
true
try
void
volatile
while

e 3 palavras reservadas: true, false e null

