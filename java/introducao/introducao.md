/**
 * Máquina virtual Java interpreta os arquivos .java e os transforma em bytecode (.class).
 * A JVM é responsável por executar o código bytecode, independente da plataforma.
 * 
 * Plataforma Java: JVM, linguagem e API
 * Closure, Ruby, Scala, Kotlin, Python, Groovy, Android? geram bytecode
 * Java é uma linguagem imperativa orientada a objetos
 * 
 * vendor lock-in
 * 
 * JRE é necessário para rodar aplicações Java
 * JDK é necessário para desenvolver. Tem o compilador Javac
 * 
 * classes só podem ser publicas, abstratas e finais
 * é possível mudar a visibilidade da classe para default.
 * nesse caso, a classe não poderá ser instanciada em outros pacotes
 * se a classe for default, ainda que seus campos e métodos estáticos sejam públicos, eles não poderão ser "vistos" de fora do pacote
 * 
 * @author a1lab
 *
 */
