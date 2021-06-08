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
13
```
* Empilhar (```push```)
```C
14 void empilha(int elemento) {
15      if(pilha.topo == tamanho){
16      printf("Fila cheia.\n");
17      system("pause");    
18      }
19      else {
20          pilha.dados[pilha.topo] = elemento;
21          pilha.topo++;
22      }    
23 }
24
```
* Desempilhar (```pop```)
```C
25 int desempilha(){
26      int elemento;
27      if(pilha.topo == pilha.ini){
28          printf("Fila vazia.\n");
29          system("pause");
30      }
31      else {
32          pilha.topo--;
33          elemento = pilha.dados[pilha.topo];
34          return elemento;
35      }
36 }
37
```
