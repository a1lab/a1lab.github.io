```java
package fundamentos;

public class Assercoes {

	/*
	 * Para aceitar asserções, é necessário habilitar por meio da VM
	 * -ea:fundamentos.Assercoes
	 */
	public static void main(String[] args) {
		assert 1 == 2 : "Erro";//uma asserção tem uma sintaxe parecida com a de um if ternário
		//contudo,  a asserção simplesmente não define nenhum comportamento para o caso da condição ser verdadeira
		//se a condição falhar, um AssertionError é disparado
	}
}

```
