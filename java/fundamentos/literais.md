
# Literais

Os literais são elementos da linguagem de programação que representam valores particulares. Java possui 5 tipos de literais:

* **Booleanos**. _true_ ou _false_.
* **Inteiros**. Exemplos: 100, 7, 365, etc.
* **Decimais**. Exemplos: 10.50, 3.14, 1.99, etc.
* **Caracteres**. 'a', 'B', 'c', 'Z', etc.
* **Cadeias de caracteres**. "Nome", "Bairro", "Valor", etc.

Os literais podem ser utilizados nas senteças de inicialização de variáveis e como argumentos de métodos, tanto de forma independente ou empregados em expressões. No exempo abaixo, na primeira sentença, os literais decimal e inteiro (respectivamente) **17.32** e **2** são empregados em uma expressão aritmética; na segunda sentença, o literal inteiro **19** é utilizado na inicialização da variável **idade**; na terceira sentença, a variável **idade** e o literal inteiro **18** são aplicados em uma expressão booleana, cujo resultado é associado à variável **maiorDeIdade**; e por fim, na última sentença, os literais **Valor da compra = R$** e **10.50** são fornecidos como argumentos ao método estático **println** da classe **System.out**.

```java
  double valor = 17.32 * 2;
  int idade = 19;
  boolean maiorDeIdade = (idade >= 18); //true
  System.out.println("Valor da compra = R$" + 10.50);
  ```
