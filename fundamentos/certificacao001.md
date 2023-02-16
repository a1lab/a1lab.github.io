# escopo de variáveis com for

* o escopo se aplica a variáveis locais
* variáveis locais têm o escopo do bloco no qual foram declaradas

* é possível declarar mais de uma variável dentro de um for, separando-as por vírgulas
* no exemplo abaixo, haverá um erro de compilação, pois as chaves estão implícitas e o escopo da variável **i** está limitado apenas à primeira linha após o for

```java
for(int i = 0 , j = 0 ; i<=10; i++) 
  j++;
  System.out.println(i);
```

> i cannot be resolved to a variable

* no exemplo abaixo, como as chaves foram explicitadas, agora o escopo de **i** abrange as duas linhas de código

```java
for(int i = 0 , j = 0 ; i<=10; i++){ 
  j++;
  System.out.println(i);
}
```

# escopo de variáveis em uma classe

* variáveis membro podem ser acessadas tanto por outros atributos e variáveis estáticas, quanto pelos métodos e construtores da classe
* variáveis estáticas podem ser acessadas tanto por meio de instâncias, quanto por meio da classe
* variáveis estáticas e de instância nao podem ter o mesmo nome
* uma variável local nao pode ter o mesmo nome de um parâmetro
* um parâmetro pode ter o mesmo nome de uma variável de instancia ou estatica
* * para fazer o acesso à variável de instância, é necessário usar **this**
* * para fazer acesso à variável de classe, é necessário usar o nome da classe
* muito cuidado com o shadowing com tipos diferentes
*  
