# Herança

* classe mãe e classe filha; superclasse e subclasse; supertipo e subtipo
* herança pode ser entre classes e entre interfaces
* um classe pode herdar o comportamento e os atributos de outra
* uma interface também pode herdar os métodos e a implementação default de outra interface
* toda classe que nao define de quem herda, herda de Object
* não existe heranca multipla em java
* só é possível ter herança se uma classe estiver visivel para a outra, assim como pelo menos um de seus construtores
* também é necessário que a classe mãe não seja final

* todos os métodos e atributos são herdados da classe mãe, independentemente da visibilidade
* contudo, a classe filha pode nao ter acesso aos membros da classe mae
* é como se a relação fosse um blueprint. No caso concreto, são classes com codigo repetido, mas a manutenção do código é centralizada

```java
public class Pessoa {
	private String documento;
	protected void setDocumento(String documento) {
		this.documento = documento;
	}
	protected String getDocumento() {
		return this.documento;
	}
}

public class PessoaFisica extends Pessoa {
	public String getCpf() {
		return getDocumento();
	}
}

```

* no exemplo acima não é possível ter acesso direto à variável documento, mas ela existe e pode ser acessada pelo método protected **getDocumento()**

# sobrescrita

* não é possível reduzir a visibilidade de um método herdado
* mas é possível aumentar a visibilidade

# redefinicao x sobrescrita

* o modificador abstract não é aceito em métodos estáticos
* é possível escrever um método na classe filha com a mesma assinatura da classe mae, contudo, trata-se de redefinicao
* a diferença ocorre não quando o método é invocado, mas quando é feito um binding de uma variavel da superclasse com uma instancia de um objeto da subclasse

```

public class Teste {
    public static void main(String[] args) {
        W w = new W();
        w.metodo(); // w

        Z z = new Z();
        z.metodo(); // z

        W zPolimorfadoComoW = z;
        zPolimorfadoComoW.metodo();
        // este último imprime w,
        // pois o binding é feito em compilação:
        // zPolimorfadoComoW.metodo é uma referencia 
        // em compilação para W
    }
}
```

# construtores e heranca

* nao existe heranca de construtores, portanto não é possível sobrescrevê-los nas classes filhas
* contudo, é possível invocá-los nas classes filhas

# sobrescrita de atributos

* não é possível remover nem sobrescrever os atributos herdados da classe mae
* é possível ter atributos com o mesmo nome, acessando-os pelos operadores **super** e **this**

# herança e exceções

* se uma classe mãe implementa um método que lança uma exceção, só é possível reecresvê-lo se lançar a mesma exceção ou um subtipo dela
* 

# ciclo

* não pode haver ciclos nas heranças
