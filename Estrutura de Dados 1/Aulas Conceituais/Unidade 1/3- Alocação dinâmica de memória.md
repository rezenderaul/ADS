# Alocação Dinâmica de Memória
* **Alocação Estática**:
    * Reserva espaço de memória em tempo de compilação.
    * pode ser mais rápida, durante a execução.
    * Pode desperdiçar memória.
* **Alocação Dinâmica**:
    * Reserva espaço de memória em tempo de execução.
    * Pode ser mais lenta, durante a execução.
    * Otimiza o uso da memória.
* Uso de memória alocada dinamicamente:
    * Tentativa de aproveitar toda a RAM disponível.
    * Cada máquina disponibiliza um espaço total de RAM de tamanho próprio.
    * Solução: alocar memória, dinamicamente, conforme a necessidade.
    * Aplicações:
        * Processadores de testo (Word).
        * Banco de dados.
    * **Biblioteca** ```stdlib.h```
    * **MALLOC()**: aloca um bloco de bytes em memória.
        * Sintaxe:
        ```C
        <ponteiro> = (<cast>*) malloc(<tamonho em bytes>);
        ```
    * **FREE()**: libera o espaço de memória alocado a uim ponteiro
        * Sintaxe:
        ```C
        free(<ponteiro>);
        ```
* **Função malloc():**
    * Responsável por vasculhar a memória e encontrar uma região que esteja livre.
    * **Casa a malloc() não consiga alocar um bloco:**
        * Retorna ```null```.
        * **Caso contrário:** retorna um ponteiro do tipo ```void``` contendo o endereço inicial do bloco.
            * Retorno do tipo ```void``` obriga um ```cast```.
    * Manipula-se o **conteúdo da variável dinâmica** com o **operador asterisco (*)**
        * **Sintaxe:**
        ``` 
        *<variável_ponteiro> = <valor>; 
        ```
    * Exemplo:
    ```C
     1 #include <stdio.h>
     2 #include <stdlib.h>
     3 int main(){
     4    int *p;
     5    p = (int *) malloc(4);
     6    if(p == NULL){
     7        printf("Erro!\n");
     8    }
     9    else {
    10      *p = 10;
    11       printf("p: %d\n", *p);
    12       free(p);
    13    }
    14 }
    ```
    * Tenho qe decorar o tamanho dos tipo primitivos? E se eu não souber qual tamanho, em bytes, utilizar?
        * Função ```sizeof()```
        * Sintaxe:
        ```C
        sizeof(<nome_do_tipo>);
        ```
        * Exemplo: utilizando a função ```sizeof()```
        ```C
         1 #include <stdio.h>
         2 #include <stdlib.h>
         3 int main(){
         4   int *p;
         5   p = (int * ) malloc(sizeof(int));
         6   if(p == NULL){
         7      printf("Erro!\n");
         8   }
         9   else {
        10      *p = 10;
        11      printf("p: %d\n", *p);
        12      free(p);
        13   }    
        14 }
        ```
## Alocar vetor dinamicamente
* Ao criar um vetor, estaticamente, é necessário especificar qual o seu tamanho:
    * Pode ocasionar desperdício de memória.
    * O vetor não pode "aumentar de tamanho" em tempo de execução.
* Sintaxe:
- 03:45
