# Tipos primitivos

* tipos primitivos guardam o valor do literal
* ao se atribuir o valor de uma variável a outra, o valor é copiado e o original não é alterado

# tipos de referencia

* com os objetos, um objeto é criado na memória e a variável aponta para esse endereço de memória
* ao atribuir uma referencia de um objeto ao valor de uma outra variável, modificar um dos dois causa uma alteração em ambos
* duas referencias são consideradas iguais para o comparador **==** se estiverem apontando para o mesmo objeto
* 

# ciclo de vida de tipos de referencia

* a criação de um objeto exige o operador new
* declarar uma variável é diferente de criar um objeto
* um objeto pode ser criado na memória, sem associá-lo a uma variável
* um objeto se torna acessível a partir do momento em que é associado a uma variável
* um objeto se torna inacessível quando a variável que fazia referencia a ele se torna nula, ou o objeto é criado sem associá-lo a uma variável
* quando o escopo de uma variável que aponta para um objeto termina, ele se torna inacessível
* todo objeto inacessível se torna disponível para o garbage collector

# garbage collector

* roda em segundo plano sem garantias de quando será executado
* só é possível determinar quantos objetos são elegíveis para a coleta, mas não quantos foram coletados


# varargs

* é possível passar um único valor, ou uma sequencia de valores, ou uma instancia de um array para o parametro do me´todo
* porém, se o método recebe um array, não é possível fornecer um varargas como parametro
* um metodo com varargs pode sobrecarregar outro com assinatura vazia, mesmo que o varargas permita receber 0 argumento. isso nao causa conflito
* 
