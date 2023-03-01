# assinatura

* a assinatura de um método tem um conjunto de modificadores, o tipo de retorno, o nome do método, um conjunto de parametros e um conjunto de exceções
* o conjunto de modificadores pode ser vazio
  * se nenhum modificador for declarado, admite-se que a visibilidade é _default_ (vísivel para o pacote)
* o tipo de retorno é obrigatório. se o método não retornar um valor ou referencia, o tipo de retorno deve ser void
* o conjunto de parâmetros pode ser vazio
* o conjunot de exceções também pode ser vazio 

E, ainda na assinatura, podemos ter:

* final - em caso de herança, o método não pode ser sobrescrito nas classes filhas;
* abstract - obriga as classes filhas a implementarem o método. O método abstrato não pode ter corpo definido;
* static - atributos acessados direto na classe, sem instâncias;
* synchronized - lock da instância;
* native - não cai nesta prova. Permite a implementação do método em código nativo (JNI);
* strictfp - não cai nesta prova. Ativa o modo de portabilidade matemática para contas de ponto flutuante.
* throws <EXCEPTIONS> - após a lista de parâmetros, podemos indicar quantas exceptions quisermos para o throws.
  
 A ordem dos elementos na assinatura dos métodos é sempre a seguinte, sendo que os modificadores podem aparecer em qualquer ordem: \<MODIFICADORES\> \<TIPO_RETORNO\> \<NOME\> (<PARÂMETROS>) \<THROWS_EXCEPTIONS\>
  
# parametros

* não é possível ter valores padrão para parametros
* se um parametro for definido na assinatura de um método, é impossível invocá-lo sem fornecer seu valor
* se um parâmetro for considerado final, não é possível modificá-lo (boa prática)
* 
  
  
