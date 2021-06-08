# Ponteiros
Como funciona a memória do computador?
* Variável -> Endereço de Memória
    * Conteúdo armazenado, fisicamente, em uma posição de memória.
* Cada tipo primitivo possui um tamanho e uma estrutura próprios, em memória:
    * Char: 1 byte
    * Int: 4 bytes
    * Float: 4 bytes
    * Double: 8 bytes
    * Bool: 1 byte

* Exemplo:
    * Declaração:
        ```C
        1 int i = 0;
        2
        3 float valor = 9.9;
        ```
    * Células de memória aglomeradas em bytes:

    | Endereço  | FFFFFFF0 | FFFFFFF4 | FFFFFFF8 |
    |-----------|:--------:| :------: | :------: |
    | Nome      | i        | valor    | **...**  |
    | Conteúdo  | 0        | 9.9      | **...**  |

* **Ponteiro - definição**: é um tipo especial de variável capaz de **armazenar endereços** de memória.
    * Um ponteiro armazena o endereço de uma outra variável.
    * Um ponteiro **aponta** para uma outra variável.
* **Utilidade de ponteiros**:
    * Quando é preciso retomar mais de um valor em função.
    * Manipulação de vetores, matrizes e strings.
    * Armazenar referências: listas, árvores, etc.
    * Alocação dinâmica de memória.
* Sintaxe de declaração de um ponteiro:
    ```C
    <tipo> * <nome_do_ponteiro>;
    ```
* IMPORTANTE
    * **Na declaração**, o operador **asterisco** (*) é o operador que **define que a variável é um ponteiro**.
    * **Fora de uma declaração**, o **asterisco** é utilizado para se trabalhar com o **conteúdo da variável para a qual o ponteiro aponta**.
    * Exemplo: declaração de um ponteiro para inteiro:
        ```C
        1 int *p;
        ```
* Operadores:
    * **& (endereço):** é utilizado quando se quer trabalhar com o **endereço de uma variável.
    * **\* (conteúdo):** é utilizado quando se quer trabalhar com o **conteúdo da variável para qual o ponteiro aponta**.
        * O **asterisco** também é utilizado na **declaração** de um ponteiro.
* **Lembre-se**: o **valor** de uma variável **é uma coisa**, o **endereço** em me,m´poria dessa mesma variável **é outra coisa** completamente diferente!
* Exemplo: considere a criação das duas variáveis a seguir:
    ```C
    1 int *p;
    2 int x;
    ```
    * Utilização do **operador de endereço (&)**:
    ```C
    3 p = &x;
    ```
    * Utilização do **operador de conteúdo (*)**:
    ```C
    4 x = *p;
    ```
* Exemplo: testando um ponteiro
```C
 1 #include <stdio.h>
 2 #include <stdlib.h>
 3 int *p;
 4 int x;
 5 int main(){
 6     x = 10;
 7     p = &x;
 8     x = 20;
 9     *p = 30;
10 }
```
* Observação importante:
    * TODO VETOR OU UMA MATRIZ, EM C, É TRATADO COMO UM PONTEIRO.
    * Considere os seguintes arrays:
    ```C
    1 int A[8];
    2 float B[4][4];
    ```