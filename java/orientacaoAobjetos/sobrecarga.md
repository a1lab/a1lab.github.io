# Sobrecarga

* dois métodos podem ter o mesmo nome, desde que tenham quantidades diferentes de parametros, ou tipos diferentes
* essa é estritaemente a unica condicao para ocorrer sobrecarga
* se os tipos de retorno forem diferentes, é impossível saber para quem invocou o método, portanto isso nao compila
* visibilidade também não faz sobrecarga
* caso haja dois métodos sobrecarregadas com tipos de referencia nos parametros, java sempre escolhe -em tempo de compilacao - o tipo mais específico
* se houver a necessidade de chamar o método da superclasse, é necessário fazer um casting explicito para o tipo mais genérico no momento da invocação do método

* o metodo abaixo compila
```java

void metodo(String i, double x) {
}
void metodo(double x, String i) {
}
```


* o metodo abaixo nao compila
```java

public class Teste {
    void metodo(int i, double x) {
    }
    void metodo(double x, int i) {
    }

    public static void main(String[] args) {
        new Teste().metodo(2, 3);
    }
}
```

* o metodo abaixo nao compila

```java

public class Xpto {
    void metodo(Object o, String s) {
        System.out.println("object");
    }
    void metodo(String s, Object o) {
        System.out.println("string");
    }

    public static void main(String[] args) {
        new Xpto().metodo("string", "string");
    }
}
```

* o método abaixo compila
```java

class Xpto2 {
    void metodo(Object o, Object o2) {
        System.out.println("object");
    }
    void metodo(String s, String s2) {
        System.out.println("string");
    }

    public static void main(String[] args) {
        new Xpto2().metodo("string", "string"); // imprime string
    }
}
```
