# Introdução à linguagem Java

> Java é tanto uma plataforma, quanto uma linguagem de programação de alto nível, simples, orientada a objetos, distribuída, dinâmica, portável, robusta, segura, performática e com múltiplas _threads_.

[Fonte: https://docs.oracle.com/javase/tutorial/getStarted/intro/definition.html]

1. Em Java, o código-fonte é primeiro escrito em uma linguagem de alto nível, em arquivos com a extensão **.java**.
2. Essas fontes são compiladas (pelo compilador **javac**) para um arquivo de _bytecodes_ com a extensão **.class**.
3. Os _bytecodes_ são interpretados pela máquina virtual **Java Virtual Machine** (também conhecida com **JVM**).
4. A **JVM** por sua vez transforma os _bytecodes_ em instruções que o sistema operacional reconhece.
5. Em suma, isso faz com que o mesmo código possa ser executado em diferentes sistemas operacionais e plataformas de _hardware_. 

![helloWorld](https://user-images.githubusercontent.com/2974552/208448650-29b58356-164b-4b82-b6a4-5a7471ed2717.gif)

[Fonte: https://docs.oracle.com/javase/tutorial/getStarted/intro/definition.html]

## Java é uma linguagem de programação orientada a objetos

* vantagem tem a ver com arquitetura cliente-servidor, comunicação, eprssitencia, rede...
* voce pode alcançar vantagems com OO impossível com procedural
* objetos tem um tempo de vida maior que funcoes

Características de uma linguagem com suporte a orientação a objetos

* Encapsulamento: esconder informação, modularização e abstração
* Polimorfismo: a mesma mensagem enviada a diferentes objetos resulta em comportamentos diferentes, dependendo da natureza dos objetos que a receberam
* Herança: novas classes são definidas com base em comportamentos de outras classes existentes, reaproveitando o c´dogio
* Ligação dinâmica (_Dynamic binding_): capacidade de enviar mensagens sem a necessidade de conhecer o tipo específico de objeto que irá recebê-las

O que são objetos

* Objetos são modelos de programação que possuem um estado interno e um comportamento
* O comportamento de um objeto é definido por seus métodos, que manipulam suas variáveis internar para alterar seu estado
* Os métodos devem ser a única maneira pela qual objetos se comunicam entre si, protengendo assim seu estado interno

O que são classes

* Uma classe define os dados/estado e métodos/comportamento de objetos que serão construídos a partir dela
* uma classe possui membros: campos e métodos
* campos armazenam dados para a classe
* métodos são sequências de instruções que operam sobre os dados da classe
* campos são específicos da instância de um objeto (variáveis de instância)
* métodos que operam sobre as variáveis de instancia são métodos de instância
* uma classe não é o objeto, mas uma planta baixa que define seu comportawmento quando ele for instanciado
* objetos podem ser obtidos instanciando classes definidias

```java
class Ponto{
  private double x;
  private double y;
  
  public Ponto(double x , double y){
    this.x = x;
    this.y = y;
  }
  
  public static void main(String args[]){
    var A = new Ponto(1,2);
    var B = new Ponto(3,4);
    var C = new Ponto(1,2);
  }
}
```

* No exemplo acima, a classe **Ponto** define as propriedades **x** e **y** dos objetos instanciados a partir dela.
* 
















