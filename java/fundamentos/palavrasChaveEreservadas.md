


## Palavras-chave e palavras reservadas

* _public_, _private_ e _protected_ são modificadores de visibilidade
* _abstract, final_ e _static_ são modificadores
* 
* _boolean, short, int, long, float, double_ e _char_ são tipos primitivos
* _throws_ é um modificador utilizado na assinatura de um método, para indicar os tipos de exceções que ele lança
* _throw, try, catch_ e _finally_ são empregadas no tratamento de exceções
* _if, else, switch, case, default, do, while, for, break_ e _continue_ são _keywords_ utilizadsa no controle de fluxo

* _true, false_ e _null_ são palavras reservadas e não podem ser utilizadas como nomes de tipos ou variáveis.


* return, void, int, byte, boolean, short, long, int, double, float, instanceof, null
* class, interface, enum, super, this, new, package, extends, implements, import
* abstract, final, static 
* assert, goto, synchronized, transient, strictfp, volatile, const, native, var

const é uma palavra reservada, mas não tem utilidade
a mesma coisa vale para goto
transient significa que o atributo não será serializado/desserializado 
volatile é usado para garantir que o valor de uma variável seja mantido na memória principal, ao invés do cache, para acesso compartilhado
synchronized é utilizado para sincronizar threads
native é utilizado apenas para métodos. Serve para criar DLLs
strictfp é utilizado para determinar pontos flutuantes em modo estrito. Isso serve para padronizar as operacoes com ponto flutuante, independente da plataforma. pq 1632 e 64 bits podem causar alterações nos resultados

* a representação binária dos tipos inteiros em java utiliza o complemento de dois com sinal
* isso vale para byte, short, int e long
