# Filas - Queue em inglês
* As filas funcionam de maneira intuitiva ao ser humano. Somos condicionados a trabalhar com filas desde pequenos.
* Funcionamento:
    * A **inserção** de elementos é feita apenas ao **fim** da fila.
    * A **remoção** de elementos só pode ser feita pela **frente** da fila.
* First in, First Out (**FIFO**)
    * Os dados são processados segundo a ordem de chegada.
* Operações com Filas:
    * Enfileirar (```push_back```)
    * Desenfileirar (```pop```)
* Atendimento de processos requisitados ao sistema operacional (escalonador).
* Alocação de recursos para impressora (Spooler de impressão).
* Ordenação do encaminhamento dos pacotes em roteador.
* Buffer para gravação de dados em mídia.
* Criando uma estrutura de dados do tipo fila
```C
 1 #include <stdio.h>
 2 #include <stdlib.h>
 3
 4 #define tamanha 3
 5
 6 struct tipo_fila{
 7      int dados[tamanho];
 8      int ini;
 9      int fim;
10 };
11
12 struct tipo_fila fila;
13
```
* Enfileirar (```push_back```)
```C
14 void enfileira(int elemento){
15      if(fila.fim == tamanho){
16          printf("Fila cheia.\n");
17          system("pause");
18      }
19      else {
20          fila.dados[fila.fim] = elemento;
21          fila.fim++;
22      }
23 }
24
```
* Desenfileirar (```pop```)
```C
25 int desenfileirar() {
26      int elemento;
27      if(fila.fim == fila.ini){
28          printf("Fila vazia.\n");
29          system("pause");
30      }
31      else {
32          elemento = fila.dados[fila.ini];
33          for(int i=0; i<tamanho; i++){
34              fila.dados[i] = fila.dados[i+1];
35          }
36          fila.dados[fila.fim] = 0;
37          fila.fim--;
38      }
39 }
40
```