# classes abstratas

* uma classe abstrata pode nao ter nenhum metodo
* se uma classe tem um método abstrato, ela deve ser declarada como abstrata, senao nao compila
* uma classe abstrata pode ter métodos abstratos e concretos
* uma classe concreta nao pode ter métodos abstratos
* uma classe abstrata nao pode ser instanciada diretamente, ou seja, nao aceita o operador new
* um metodo abstrato é um método sem corpo, somente com uma definicao

# herança entre classes abstratas

* se uma classe cocnreta herda de uma abstrata, ela deve obrigatoriamente implementar todos os métodos abstratos
* se uma classe abstrata herda de uma abstrata, ela pode implementar alguns métodos abstratos

```java
abstract class Pai {
	abstract void metodoAbstrato();
	abstract void outroMetodo();
}

abstract class Filha extends Pai{
	void metodoAbstrato() {
	}
}

public class Neta extends Filha{
	void outroMetodo() {
	}
}
```

* no exemplo acima, a classe pai define dois métodos abstratos, a classe filha implementa um deles, e a classe neta o outro
* a classe filha poderia implementar ambos, evitando que a classe neta tenha que fazê-lo
* a classe neta poderia sobrescrever o método implementado pela classe filha
* se a classe filha não implementasse nenhum deles, deveria ser abstrata. Dessa forma a classe neta precisaria implementar ambos
* quando herdamos de uma classe abstrata, herdamos suas responsabilidades, dessa forma, ou implemetamso esses métodos ou passamos adiante, o que exigiria tornar a classe abstrata
* 
