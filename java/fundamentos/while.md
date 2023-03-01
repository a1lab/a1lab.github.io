# DO WHILE

* no caso do DO WHILE, a condição é testada após a execução do corpo do laço, pelo menos uma vez

```java
int i = 1;
do { //executa ao menos 1 vez
    System.out.println(i);
    i++;
} while (i < 10); // se der true, volta e executa novamente.
```

* o ponto e vírgula após o while é obrigatório


```java
class A {
    public static void main(String[] args) {
        int i = 0;
        do System.out.println(i); while(i++>10);
    }
}
```
