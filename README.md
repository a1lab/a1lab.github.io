# a1lab.github.io

```java
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

---
title: Animal example
---
classDiagram
    note "From Duck till Zebra"
    Animal <|-- Duck
    note for Duck "can fly\ncan swim\ncan dive\ncan help in debugging"
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
