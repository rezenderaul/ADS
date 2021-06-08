# Pilhas - Stack em inglês
* Definição de pilha:
    * Lista linear em que todos os **acessos** se dão em uma **única extremidade** da estrutura de dados - o **topo** da pilha.
    * Imagine uma pilha de livros, de pratos.
* Conceito:
    * Last In, First Out (**LIFO**): O último a entrar, será o primeiro a sair.
    * Os **elementos** só podem serem **inseridos** no **topo**. É só podem ser **retirados** pelo **topo**.
    * Funções:
        * ```push(elemento)``` - Empilhar no topo.
        * ```pop()``` - Remove elemento do topo.
* **Aplicações**
    * Avançar e voltar em navegadores.
    * Desfazer e refazer em editores.
    * Recursividade.
    * Chamadas e execução de funções.
* **Operações sobre pilhas**
    * Empilhar (```push```)
    * Desempilhar(```pop```)
* Criando uma estrutura de dados do tipo pilha
```C
 1 #include <stdio.h>
 2 #include <stflib.h>
 3
 4 #define tamanho 3
 5
 6 struct tipo_pilha{
 7      int dados[tamanho];
 8      int ini;
 9      int topo;
10 };
11
12 struct tipo_pilha pilha;