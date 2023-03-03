# Polimorfismo

```java

class Veiculo {
    public void liga() {
        System.out.println("Veiculo está sendo ligado!");
    }
}

class Carro extends Veiculo {
    public void liga() {
        System.out.println("Carro está sendo ligado!");
    }
}


public class Teste{
    public static void main(String [] args){
        Veiculo v = new Carro();
        v.liga();
    }
}

```

* no exemplo acima, o método invocado será o da classe Carro, independnete da variavel ser do tipo veículo
* isso é decidido em tempo de execucao

* para reescrever um nome é necessário ter o mesmo nome, mesmos parametros, mesmo tipo de retorno, visibilidade igual ou menos restritiva, exceptions iguais e o método na superclasse não deve ser final
  * o tipo de retorno, se for de referencia, pode ser um subtipo do tipo de retorno da classe mae
  * as exceções também podem ser subtipos

* um método herdado pode ser sobrescrito com um método abstrato, escondendo a implementação da superclasse e exigindo uma implementação de quem herdar do subtipo
* todo método de uma interface é publico por padrao


# retorno covariante

* um método sobrescrito em uma classe filha pode ser do mesmo tipo ou mais específico na classe filha
* isso só vale pra tipos de referencia, e nao para tipos primitivos

# exceções

* um método sobrescrito só pode lançar as mesmas exceções checked ou exceções mais específicas
* em relação às unchecked, não há restriç]oes
* se a exceção for mais genérica, o codigo nao compila

#sobrescrita de métodos

```java

Veiculo v = new Carro();
v.liga(); // ligando o carro?
v.desliga();
```

* Vamos linha por linha: primeiro, podemos chamar um Carro de Veiculo porque ele é um (compila sem problemas). Podemos também chamar o método liga pois ambas as classes o possuem. Mas o método que será invocado será o da classe filha, o sobrescrito.

Já a chamada ao método desliga não compilará, porque ele não está definido na classe Veiculo. Como a referência é desse tipo, o método (que existe no objeto) não é visível.


# super

* em um método sobrescrito, é possível invocar o método da classe mãe, por meio do operador super
