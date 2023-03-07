* às vezes temos referências de um tipo, mas sabemos que a instância é de outro objeto

```java
public class Teste{
    public static void main(String...args){
        Object[] objetos = new Object[100];

        String s = "certificacao";
        objetos[0] = s;

        String recuperada = (String) objetos[0];
    }
}
```

* o código acima compila, mas durante a execução a JVM vai realizar o casting e verificar se é possível fazer tal conversão
* se não for compatível, lança uma ClassCastException

```java
    class Veiculo {}
    class Moto extends Veiculo {}
    class Carro extends Veiculo {}
    
    Veiculo v = new Carro();
    Moto m = v;
```

* como um carro é um veículo, o polimorfismo funciona
* ao tentar converter um veiculo, que contém uma referência de um carro, para uma moto, ocorre um erro, pois nem veículo é uma moto
* dessa forma, nem forçando o casting isso vai compilar

```java
    Veiculo v = new Carro();
    Moto m = (Moto) v;
```

* quando o casting é opcional, o códgio compila com ou sem o casting
* se vc estiver subindo na hierarquia de classes, a autopromocao faz o trabalho sozinho
* se vc estiver descendo, é necessário delcarar o casting explícito
* não é possível migrar para um caminho irmaõ no casting

# casting com interfaces

* ao criar uma classe que implementa uma interface, ao tentar fazer o casting, o compilador aceita, mas em tempo de execução ocorre uma classcastexception

# classes final

* se uma classe for final, o compilador reconhece em tempo de compilação que ela nao pode ser estendida e gera um erro de compilacao

# instanceof

* se a referencia for compativel, o código compila e retorna false em tempo de execução
* se o compilador puder verificar em tempo de execução que as instancias não sao compativeis, o códgio nem compila
* instanceof deve ser evitado. Em geral ele indica uma modelagem fraca
