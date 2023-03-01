* break interrompe o laço do seu bloco
* continue pula a iteração atual, mas nao interrompe o laço
* se houver um laço infinto com um break, o código é compilável
* break e continue podem ser aplicados tanto em while, do-while e for

# label

* um label pode ser colocado antes de qualquer instrução
* um break ou continue só pode ser usado com um label, se o label fizer referencia a um laço
* um break ou continue com label só funciona se referenciar o proprio laco

```java
    void rotuloEmOutroLaco() {
        rotulo:
        for(int i=0;i<10;i++) {
            System.out.println("oi");
        }
        for(int i=0;i<10;i++) {
            break rotulo; // não compila
        }
    }
```

* um label pode ser repetidos em laços separados diferentes
* se os laços estiverem aninhados, os labels devem ser diferentes

```java

    void rotulosRepetidos() {
        rotulo: for (int i = 0; i < 10; i++) {
            break rotulo;
        }
        rotulo: for (int i = 0; i < 10; i++) {
            break rotulo;
        }
    }
    void rotulosRepetidosNestedNaoCompila() {
        rotulo: for (int i = 0; i < 10; i++) {
            rotulo: for (int j = 0; j < 10; j++) {
                break rotulo;
            }
        }
    }
```

* não há conflito de nomes de variáveis e rótulos, pois o uso é diferente eo compilar sabe disso
* um statement pode ter mais de um label

```java

    void rotulosNoMesmoStatement() {
        primeiro: segundo: for (int i = 0; i < 10; i++) {
            System.out.println(i);
        }
    }
```

