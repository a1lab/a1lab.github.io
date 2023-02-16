# Criando e executando uma aplicação com Main

* java c <nomedoarquivo.java> para compilar
* java <nomedoarquivo> para executar
* se for necessário passar argumentos para o programa, isso deve ser feito por uma lista separada por espaços simples
* java <nomedoarquivo> <param1> <param2>
  * o JRE tem a JVM e permite executar o comando java, para executar programas java
  * o JDK tem o compilador javac, que permite compilar programas java
* se um arquivo estiver em um diretório separado, deve-se usar o pacote para organizar o namespace
* para passar o valor de uma propriedade para o programa, deve-se colocar o valor entre o comando java e o nome do arquivo
  
```
  javac MinhaClasse.java
  java -Dambiente=desenvolvimento -Dtestes=skip MinhaClasse
```
  
* a classe não precisa ser publica para o método main ser executado
  
* se os arquivos estiverem em outro diretório:
  
```java
  package outroDiretorio;
  
  class MinhaClasse{
    public static void main(String[] args){
  
    }
  }
```
  
```
  javac outroDiretorio/MinhaClasse.java
  java outroDiretorio.MinhaClasse
```
