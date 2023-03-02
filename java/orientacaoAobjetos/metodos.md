# Métodos

* Classes, enums e interfaces podem ter métodos
* Todo método tem uma assinatura e pode ter um corpo, se não for abstrato
* A assinatura contém
  * Um modificador de visibilidade (se omitido, é _default_, ou de pacote)
  * Outros modificadores como _final, abstract, static, synchronized, native e strictfp_ 
  * Um tipo de retorno. Se não houver retorno, o tipo deve ser explitamente definido como void
  * O nome do método
  * Uma lista ordenada de parâmetros, se houver
  * Uma lista ordenada de exceções, se houver

> \<MODIFICADORES\> \<TIPO_RETORNO\> \<NOME\> (\<PARÂMETROS\>) \<THROWS_EXCEPTIONS\>

* A lista de parâmetros deve incluir o tipo do parâmetro e deve ser separada por vírgulas
* Não é possível ter valores padrão para os parâmetros
* A inicialização dos parâmetros é feita durante a chamada. Assim, dentro dos métodos, os parâmetros sempre estão inicializados
* Não é possível invocar um método sem fornecer o valor de um parâmetro
* Se o paâmetro for final, não é possível alterar seu valor (boa prática)

# Promoção de parâmetros

## Promoção de parâmetros de tipos primitivos
* Parâmetros também estão sujeitos à promoção de tipos primitivos e polimorfismo
* Se um parâmetro for de um tipo e quem o invocou fornecer um tipo menor, o valor é promovido para o tipo do parâmetro implicitamente
  * Dessa forma, dentro do método, o desenvolvedor pode assumir que o tipo do parâmetro é sempre do tipo da assinatura 
* Se o valor fornecido for maior, é necessário fazer um casting durante a invocação do método

## Promoção de parâmetros de tipos de referência
* Se um método tem um parametro de um tipo em sua assinatura, é possível fornecer qualquer subtipo dele na invcação
  * COntudo, dentro do método, esse parâmetro sempre será tratado como sendo do tipo especificado na assinatura

# Retorno de valores
* Todo método deve retornar algo: um tipo primitivo ou um tipo de referência
* Se o método não retornar nada, o tipo de retorno deve ser definido como _void_
* Se o tipo de retorno for _void_, a instrução _return_ pode ser omitida
* Nesse tipo de situação, é possível ter um retorno antecipado, interrompendo o fluxo de execução
* Também nesse caso, não é possível ter nenhuma instrução após o retorno antecipado, causando um problema de compilação

* Todo método que retorna algo, deve retornar um valor, ou lançar uma exceção em cada ramificação do fluxo de execução
* Caso contrário, o código não compila
* 
* Métodos que não retornam nada, não podem ser atribuidos a outras variáveis
* Se um método retorna algo, seu retorno pode ser ignorado
