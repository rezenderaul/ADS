# Revisão 
## Algorítimo e Logica de programação 2  
### Vetores
Também são conhecidos como:
* Arranjo
* Array
* Agregado homogêneo unidimensional  

São matrizes de uma única linha  

Em linguagem C:
* São declarados de maneira similar a uma variável comum, porém, adiciona-se o tamanho
* Têm um tamanho máximo N
* O primeiro elemento encontra-se na posição 0
* O último elemento encontra-se na posição N-1  

Sintaxe de declaração de um vetor:  
``` C 
<tipo> <nome> [<tamanho>]  
```

Declaração com lista de inicialização:
``` C 
<tipo> <nome> [<tamanho>]={<v1>,<v2>,...,<vN>};  
```

Exemplo: 
``` C
int B[3]={15, 66, 42};
```

Sintaxe para acesso aos elementos de vetor:
``` C
<nome_do_vetor>[<índice>];
```

### Matrizes
Definição matemática: uma matriz é um arranjo tabular de MxN valores, onde M é o número de linha e N é o número de colunas.  
Os elementos de uma matriz são acessados por dois índices:  
* i - geralmente associados às linhas
* j - geralmente associados às colunas
Índices variam de 0 a M-1 e de 0 a N-1.  

* Sintaxe de declaração de uma matriz
``` C 
<tipo> <nome>[<dim1>][<dim2>]...[<dimN>];
```

* Exemplo de criação de uma matriz bidimensional:
``` C 
int A[3][3]
```

* Sintaxe de acesso a um elemento da matriz:
``` C 
<nome_da_matriz>[<índice1>][<índice2>]...[<índiceN>]
```

* Exemplo de acesso a elementos da matriz:
``` C 
A [0][0];
A [2][2];
A [0][2];
A [1][0];
```

### Estruturas de dados heterogêneas:
Também conhecidos como registros, tipos de dados compostos, ```structs```.  
* Em linguagem C:
    * Agrupam informações de tipos de dados diferentes
    * Trata de um grupo de valores como sendo uma única variável com vários campos distintos
    * Cria-se um novo tipo de dados

* Registro em linguagem C:
  * Sintaxe de definição:
    ``` C
    struct <nome_do_registro> {
        <tipo> <nome_do_campo1>
        <tipo> <nome_do_campo2>
        ...
        <tipo> <nome_do_campoN>
    };
    ```
* Esta é a declaração de um novo registro, reconhecido por ```<nome_do_registro>```

    * Como utilizar uma ```struct```?
      * Apenas definir a ```struct``` não basta
      * É preciso criar uma variável do novo tipo criado
    * Sintaxe para criação de uma variável do tipo ```struct```:
    ``` C
    struct <nome_do_registro> <nome_da_variável>
    ```
    * Exemplo
      ``` C
      struct produto p1;
      ```
    * Acesso aos dados de um registro
      * Utiliza-se o nome da variável estática do registro seguida de um ponto(.), e então referencia-se o campo desejado.
    * Sintaxe:
    ```C
    <name_da_variável>.<campo>
    ```
    * Registros podem ser combinados com vetores:
     i. Declara-se um novo registro
     ii. Cria-se um vetor de registros (assim como se cria uma variável do tipo registro)
    * Exemplo: criar uma lista de produtos
      * Vetor de registro do tipo "produto"