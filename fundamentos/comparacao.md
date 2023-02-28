# Comparação entre strings

```java
System.out.println("Mario"=="Mario");
```

>true

* No exemplo acima, a JVM cria um objeto do tipo String, com o valor **Mario** e aloca tal valor no pool de strings
* Em seguida, ao realizar a comparação, a JVM recupera a referência desse objeto e compara duas referências idênticas, resultando em  **true**


```java
String nome1 = new String("Mario");
String nome2 = new String("Mario");
System.out.println(nome1 == nome2);

```
> false

* Nesse segundo exemplo, embora o conteúdo das strings seja o mesmo, são criados dois objetos no pool de strings
* A comparação é feita entre referências diferentes, resultando em **false**

```java
String nome1 = "Mario";
String nome2 = "Mario";
System.out.println(nome1 == nome2);
```

> true

* No último exemplo, na declaração da variável **nome1**, a JVM cria uma string cujo valor é **Mario**.
* Na segunda linha, ao declarar e inicilizar a variável **nome2**, a JVM associa a ela o mesmo valor **Mario**
  * Para isso, a JVM recupera a referência da primeira string do pool de strings e associa à segunda variável
  * Dessa forma, ambas as variáveis apontam para a mesma referência
  * Ao compará-las, o resultado será **true**. 

* Para verificar se o conteúdo de duas strings é o mesmo, deve-se usar **equals** ao invés do operador **==**.

```java

String ab = "a" + "b";
System.out.println("ab" == ab); // true
```
> true

* no exemplo acima, serão criadas três strings na primeira linha: **a**, **b** e **ab**
* nessa mesma linha a variável **ab** será associada à string **ab**, do pool de strings
* na segunda linha, o teste retornará verdadeira, pois a comparação acontece entre a mesma referência

```java
String a = "a";
String ab = a + "b"; //usando uma referência e um literal
System.out.println("ab" == ab); // false
```

> false

* nesse outro exemplo, a string **a** será criada na primeira linha e associada à variável **a**
* na segunda linha, uma nova string será criada (**b**)
* ainda na segunda linha, a concatenação entre a string **b** e a variável **a** vai gerar uma nova string **ab**
* na terceira linha, a declaração do literal **ab** vai criar uma nova string, de modo que a comparação vai retornar **false**

# string são imutáveis

```

String str = "um texto qualquer";
String txt1 = "texto";
String txt2 = str.substring(3, 8); //cria uma nova string com valor "texto"
System.out.println(txt1 == txt2); // false
System.out.println(txt1.equals(str.substring(3, 8))); // true, pois a comparação é feita entre os valores
```

```java

String str = "HELLO WORLD";
String upper = str.toUpperCase();          // já está maiúscula
String subs = str.substring(0,11);         // string completa
System.out.println(str == upper);          // true
System.out.println(str == subs);           // true
System.out.println(str == str.toString()); // true

```

* se o resultado de uma transformação em uma string for a própria string original, nenhum novo objeto é criado no pool

# teste de igualdade com equals

* Para comparar objetos, mesmo que dois objetos tenham os mesmos valores para suas propriedades, ao utilizar o operador **==**, o resultado será **false**
* Isso acontece, pq a comparação feita pela JVM é feita entre as referências. Se forem diferentes, o resultado será falso
* Utilizar o método **equals** também não resolve o problema, pois por padrão o equals -herdado de object- faz uma comparação usando o operador **==**
* Para solucionar o problema é necessário sobrescrever o método **equals(Object)**
  * Percebe que, sobrecarregar o método com outro tipo de referência não sobrescreve o objeto original
  * Isso funciona em alguns casos, mas gera efeitos colaterais em outros, como nas implementações das coleções java 


