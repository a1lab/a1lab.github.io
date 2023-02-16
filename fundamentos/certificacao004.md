# importação de outros pacotes

* se duas classes estão no mesmo pacote, não é necessário importá-las
* ao compilar uma classe que depende de outra, do mesmo pacote, o compilador compila ambas
* **não é possível importar classes do pacote padrao**, mesmo que a classe seja publica
* por isso, nunca se deve colocar classes no pacote default
* toda importação deve ser feita assim \<nomedopacote\>.\<nomedaClasse\>
* a importação **import .\*** importa os tipos contidos no diretório, mas não importa os subpacotes nem os subtipos
* como fazer a importacao de classes aninhadas?
* e os import static?


* o exemplo abaixo gera erro, pois há um import de dois tipos com o mesmo nome, mas de pacotes diferentes, causando ambiguidade

```java
import modelo.basico.Cliente;
import modelo.avancado.Cliente;
```

* o exemplo abaixo **nao** gera erro, pois trata-se do mesmo import. A instrução é redundante e gera um warning, mas compila

```java
import modelo.basico.Cliente;
import modelo.avancado.Cliente;
```

* No exemplo abaixo, se houver duas classes com o mesmo nome em pacotes diferentes, também não há erro, pois o import específico tem precedencia sobre o asterísco

```java
import modelo.basico.Cliente;
import modelo.avancado.*;
```



  
                                                                   
  
  

