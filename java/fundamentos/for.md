# Estrutura do laço

```java
int i = 1; // Inicialização
while (i < 10) { // Condição
    System.out.println(i); // Comandos
    i++; // Atualização
}
```

# FOR

* inicialização, condição e atualização no for são opcionais !

```java
for(;;){
    // CODIGO
}

for(;true;){
    // CODIGO
}

//a cada volta do laço, incrementamos o i e decrementamos o j
for (int i=1,j=2;; i++,j--){
    //código
}
```

* só não é possível declarar variáveis de tipos diferentes na inicilaização

```java
for (int i=1, long j=0; i< 10; i++){ // erro
    //código
}
```

* no campo de incremento é possível executar qualquer tipo de instrucao

```java
class A {
    public static void main(String[] args) {
        for(int i=0; i<2; i++, System.out.println(i)) {
            System.out.println(i);
        }
    }
}
```

* o codigo abaixo nao compila, pois ha uma tentativa de definir dois tipos dentro do mesmo for

```java

class A {
  public static void main(String[] args) {
    for(int i=0, int j=1; i<10; i++, j++) System.out.println(i);
 }
}
```

# enhanced for

* so vale para percorrer colecoes. se a coleção nõa é ordenada, 

```java
int[] numeros = {1,2,3,4,5,6};
for (int num : numeros) { //enhanced for
    System.out.println(num);
}
```

* ao usar essa forma de FOR, a variável criada é um novo objeto, ou seja, alterá-la não altera a coleção original

```

ArrayList<String> nomes = new ArrayList<>();
nomes.add("Joao");
for (String nome : nomes) {
    nome = null;
}
for (String nome : nomes) {
    System.out.println(nome);
}
```

> João

