

```



## Outras notações

```java
  int valorHexadecimal = 0x1a;
  int valorOctal = 075;
  int valorBinario = 0b110011;
  int valorDecimal = 26;
```  
  
```java
  int valorEmNotacaoCientifica = 1.2457e4; // 1.2457 * 10^4
```

```java
  
```

* Não é permitido colocar um _underscore_ no início, nem no fim de um literal numérico (inteiro ou decimal).
* Não é possível colocá-lo adjacente ao ponto decimal de um literal decimal.
* Também não é possível colocá-lo entre o valor numérico de um literal e os indicadores de tipo *long, float* ou *double* (L, F ou D, respectivamente).
* Por fim, também é proibido colocá-lo entre os caracteres que indicam as notações binária, hexadecimal e científica.

Todos as sentenças do exemplo abaixo causam erros de compilação, em virtude das restrições acima descritas.

```java
  int inteiroUnderscoreNoInicio = _10;
  int inteiroUnderscoreNoFim = 10_;
  double decimalUnderscoreNoInicio = _10.5;
  double decimalUnderscoreNoFim = 10.5_;
  double underscoreAntesDoPontoDecimal = 10_.5;
  double underscoreDepoisDoPontoDecimal = 10._5;
  long inteiroUnderscoreAntesDoIndicadorDeTipo = 10_L;
  float decimalUnderscoreAntesDoIndicadorDeTipo = 10.5_F;
  byte byteUnderscoreEntreCaracteresDeNotacao = 0_b0001;
  int hexdecimalUnderscoreEntreCaracteresDeNotacao = 0_x0001;
```

Os exemplos abaixo, por outro lado, representam casos aceitos

```java
  long creditCardNumber = 1234_5678_9012_3456L; 
  long socialSecurityNumber = 999_99_9999L; 
  float pi = 3.14_15F; 
  long hexBytes = 0xFF_EC_DE_5E; 
  long hexWords = 0xCAFE_BABE; 
  long maxLong = 0x7fff_ffff_ffff_ffffL; 
  byte nybbles = 0b0010_0101; 
  long bytes = 0b11010010_01101001_10010100_10010010;
```
