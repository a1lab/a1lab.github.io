# Passagem de parâmetros

* java guarda todas as chamadas de parâmetros em um pilha, e os objetos que foram criandos, no heap
* a passagem de parametros em java é feita por cópia de valores
* dessa forma, alterações nos valores dos parâmetros não afetam os valores das variáveis locais em outros trechos do código

## Passagem de tipos primitivos

```java

class Teste {
    public static void main(String[] args) {
        int i = 2;
        teste(i);
        System.out.println(i); 
    }

    static void teste(int i) {
        i = 3;
    }
}
```

## Passagem de tipos de referência

```java

class Pessoa {
  public int idade = 18;

    public static void main(String[] args) {
        Pessoa pessoa = new Pessoa();
        System.out.println(pessoa.idade);
        alteraIdade(pessoa);
        System.out.println(pessoa.idade);
        anulaPessoa(pessoa);
        System.out.println(pessoa.idade);
        pessoa = null;
        System.out.println(pessoa.idade);
    }

    static void alteraIdade(Pessoa pessoa) {
        prova.idade = 21;
    }
    
    static void anulaPessoa(Pessoa pessoa){
        pessoa = null;
    }
}
```
> 18
>
> 21
> 
> 21
>
> NullPointerException

* No exemplo acima, uma cópia da referência para o objeto pessoa é passada para os métodos estáticos
* Dessa forma, eles são capazes de alterar os atributos da mesma referência
* Por outro lado, eles são incapazes de anular o objeto original
* Dentro de um método, associar um parâmetro a uma nova de referência de outro objeto não vai causar a alteração no objeto original

class Pessoa {
  public int idade = 18;

    public static void main(String[] args) {
        Pessoa pessoa = new Pessoa();
        System.out.println(pessoa.idade);
        mudaPessoa(pessoa);
        System.out.println(pessoa.idade);
    }

    static void mudaPessoa(Pessoa pessoa) {
        pessoa = new Pessoa();
        pessoa.idade = 99;
    }
}
```
> 18
>
> 18

