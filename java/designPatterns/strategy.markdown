# Strategy

## Descrição do problema recorrente

```java
class Orcamento {

	private BigDecimal valor;
	
	public Orcamento(BigDecimal valor) {
		this.valor = valor;
	}
	
	public BigDecimal getValor() {
		return this.valor;
	}
	
}
```


```java
enum TipoImposto {
	ICMS, ISS
}
```

```java
class CalculadoraDeImpostos{
  BigDecimal calcular(Orcamento orcamento, TipoImposto tipoImposto){
    switch(tipoImposto){
      case ICMS:
        return orcamento.getValor().multiply(new BigDecimal("0.1"));
        break;
      case ISS:
        return orcamento.getValor().multiply(new BigDecimal("0.06"));
        break;
      default:
        return BigDecimal.ZERO;
    }
  }
}

```

## Solução

```java
interface TipoImposto {
	BigDecimal calcular(Orcamento orcamento);
}
```

```java
class CalculadoraDeImpostos{
  BigDecimal calcular(Orcamento orcamento, Imposto imposto){
    return imposto.calcular(orcamento);
  }
}

```

```java
class ISS implements ImpostoInterface {
	public BigDecimal calcular(Orcamento orcamento) {
		return orcamento.getValor().multiply(new BigDecimal("0.06"));
	}
}	
```

```java
class ICMS implements ImpostoInterface {
	public BigDecimal calcular(Orcamento orcamento) {
		return orcamento.getValor().multiply(new BigDecimal("0.1"));
	}
}
```
