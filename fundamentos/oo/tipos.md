# diferencie tipos de referencia de tipos de objetos

* sempre que estendemos uma classe ou implementamos uma inteface, criamos um relacionamento **é um**
* quando criamos uma instancia de um objeto e o associamos a uma classe ou interface de outro tipo, fazemos uso do polimorfismo

```java
    Veiculo v = new Carro();
    List l = new ArrayList();
```

* herança e implementação formam uma árvore cuja raiz é a classe Object
* a maior vantagem do uso de polimorfismo vem da passagem de parametros
* se um método recebe um parametro de um supertipo, podemos passar qualquer subtipo a ele

```java
class Carro{}
class Moto{}
class Onibus{}
class Caminhao{}

void calculaPedagio(Carro carro){}
void calculaPedagio(Moto moto){}
void calculaPedagio(Onibus onibus){}
void calculaPedagio(Caminhao caminhao){}
```

* o exemplo acima usa sobrecarga de métodos, mas não usa polimorfismo
* no exemplo abaixo, substituimos a implementacao dos quatro métodos, por um único com polimorfismo

```java
abstract class Veiculo{}
class Carro extends Veiculo{}
class Moto extends Veiculo{}
class Onibus extends Veiculo{}
class Caminhao extends Veiculo{}

void calculaPedagio(Veiculo veiculo){}

calculaPedagio(new Carro());
```

* podemos referenciar um ojbeto (associá-lo a uma variável) por meio de seu tipo, ou qualquer um de seus supertipos ou interfaces que ele implementa
* ao fazer isso, abrimos mão de acessar os métodos e atributos da classe filha, pois o compilador não conhece tais métodos em tempo de execução
* se o método não foi definido na classe de referência (da variável), o códgio não compila

* se a classe pai está em um pacote diferente e têm métodos _default_, não é possível acessá-los
  * para isso, é necessário torná-los púlbico ou _protected_

* se houver sobrescrita de métodos, o método da classe filha deve ser mais restritivo ou ter a mesma visibilidade do da classe pai
  * caso contrário, não haverá sobrescrita, mas redefinição e isso vai afetar o binding feito pelo compilador no momento de invocar tais métodos

```java 
package financeiro;
public class ContaFinanceira extends modelo.Conta {
    public void fecha() {
        System.out.println("fechando financeiro");
    }
}

package modelo;
public class Conta {
    public void fecha() {
        System.out.println("fechando conta normal");
    }
}

package codigo;
import financeiro.*;
import modelo.*;
class A {
    public static void main(String[] args) {
        Conta c = new ContaFinanceira();
        c.fecha();
    }
}
```

> Compila e roda, imprimindo fechando financeiro.
