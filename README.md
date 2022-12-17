# a1lab.github.io

```
public static void main(String[] args) {
		int valor;
		Classes classes = new Classes();
		System.out.println(classes.teste);
		System.out.println(classes.caractereZero);

		Classes primeiraClasse = new Classes(); // a parte direita da declaração cria um objeto
		// a esquerda referencia à variável primeiraClasse, do tipo Classes
		primeiraClasse.teste = true;
		Classes segundaClasse = primeiraClasse;
		// ao fazer isso, a variável segundaClasse aponta para o mesmo objeto de
		// declaração acima
		// toda alteração em uma variável afeta a outra
		primeiraClasse.teste = false;
		System.out.println(segundaClasse.teste + " deve ser false");
		segundaClasse.teste = true;
		System.out.println(primeiraClasse.teste + " deve ser true");

	}
```
