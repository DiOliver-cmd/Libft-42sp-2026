# Libft - Sua primeira biblioteca.

## 📝 Descrição
O projeto **Libft** consiste na criação de uma biblioteca em C que agrupa diversas funções de uso geral que serão utilizadas em futuros projetos da escola. O objetivo central é compreender o funcionamento interno de funções padrão da biblioteca `libc`, reimplementando-as do zero para desenvolver fundamentos sólidos em programação e manipulação de memória.

## 🛠️ Instruções
### Compilação
A biblioteca é compilada gerando um arquivo chamado **`libft.a`** na raiz do repositório. O `Makefile` incluído utiliza o compilador `cc` com as flags de erro obrigatórias:
```bash
make          # Compila as funções obrigatórias
make bonus    # Compila as funções de lista encadeada (Parte 3)
make clean    # Remove arquivos objeto (.o)
make fclean   # Remove arquivos objeto e a biblioteca .a
make re       # Realiza o fclean e compila novamente
```
**Nota:** O Makefile não realiza *relink* desnecessário e todos os arquivos fonte são **explicitamente nomeados**, conforme exigido pela Norma.

## 📚 Conteúdo da Biblioteca
As funções estão organizadas em três blocos principais, subdivididas por categoria de operação:

### **Bloco 1: Funções da Libc (Reimplementações)**
Nesta parte, as funções seguem rigorosamente o comportamento descrito em suas respectivas `man pages`.

*   **Tipo: Verificação e Conversão de Caracteres**
    *   `ft_isalpha`: Verifica se o caractere é alfabético.
    *   `ft_isdigit`: Verifica se o caractere é um dígito.
    *   `ft_isalnum`: Verifica se o caractere é alfanumérico.
    *   `ft_isascii`: Verifica se o caractere pertence à tabela ASCII.
    *   `ft_isprint`: Verifica se o caractere é imprimível.
    *   `ft_toupper`: Converte um caractere para maiúsculo.
    *   `ft_tolower`: Converte um caractere para minúsculo.

*   **Tipo: Manipulação de Memória**
    *   `ft_memset`: Preenche a memória com um byte constante.
    *   `ft_bzero`: Zera uma porção de memória.
    *   `ft_memcpy`: Copia uma área de memória (sem sobreposição).
    *   `ft_memmove`: Copia uma área de memória (com segurança para sobreposição).
    *   `ft_memchr`: Localiza um caractere em um bloco de memória.
    *   `ft_memcmp`: Compara dois blocos de memória.
    *   `ft_calloc`: Aloque e zera a memória de forma dinâmica.

*   **Tipo: Manipulação de Strings**
    *   `ft_strlen`: Calcula o comprimento de uma string.
    *   `ft_strlcpy`: Copia strings com limite de tamanho.
    *   `ft_strlcat`: Concatena strings com limite de tamanho.
    *   `ft_strchr`: Localiza a primeira ocorrência de um caractere na string.
    *   `ft_strrchr`: Localiza a última ocorrência de um caractere na string.
    *   `ft_strncmp`: Compara duas strings até um limite de caracteres.
    *   `ft_strnstr`: Localiza uma substring dentro de outra string.
    *   `ft_strdup`: Duplica uma string usando alocação dinâmica.

*   **Tipo: Conversão de Dados**
    *   `ft_atoi`: Converte uma string para um número inteiro.

---

### **Bloco 2: Funções Adicionais**
Funções que não constam na `libc` ou possuem implementações específicas para o projeto.

*   **Tipo: Manipulação de Strings Avançada**
    *   `ft_substr`: Cria uma substring a partir de uma string original.
    *   `ft_strjoin`: Concatena duas strings em uma nova alocação.
    *   `ft_strtrim`: Remove caracteres específicos do início e fim de uma string.
    *   `ft_split`: Divide uma string em um array de strings usando um delimitador.
    *   `ft_strmapi`: Aplica uma função a cada caractere de uma string (gera nova string).
    *   `ft_striteri`: Aplica uma função a cada caractere de uma string (modifica a original).

*   **Tipo: Conversão de Dados**
    *   `ft_itoa`: Converte um número inteiro para uma string.

*   **Tipo: Saída em File Descriptors (FD)**
    *   `ft_putchar_fd`: Escreve um caractere no FD especificado.
    *   `ft_putstr_fd`: Escreve uma string no FD especificado.
    *   `ft_putendl_fd`: Escreve uma string seguida de nova linha no FD.
    *   `ft_putnbr_fd`: Escreve um número inteiro no FD especificado.

---

### **Bloco 3: Funções de Listas Encadeadas (Bônus)**
Funções para gerenciar a estrutura `t_list`, composta por `void *content` e `struct s_list *next`.

*   **Tipo: Gerenciamento de Nós e Lista**
    *   `ft_lstnew`: Cria um novo nó de lista.
    *   `ft_lstadd_front`: Adiciona um nó no início da lista.
    *   `ft_lstsize`: Conta o número de elementos da lista.
    *   `ft_lstlast`: Retorna o último nó da lista.
    *   `ft_lstadd_back`: Adiciona um nó no final da lista.
    *   `ft_lstdelone`: Deleta um único nó e limpa seu conteúdo.
    *   `ft_lstclear`: Deleta uma lista inteira e seus sucessores.
    *   `ft_lstiter`: Itera sobre a lista aplicando uma função a cada conteúdo.
    *   `ft_lstmap`: Cria uma nova lista resultante da aplicação de uma função em cada nó.

---

## 📜 Regras da Norma
O código respeita integralmente a **Norma v4.1 da 42**:
*   Limite de **25 linhas** por função.
*   No máximo **5 variáveis** por função.
*   Proibição do uso de `for`, `do...while`, `switch`, `case`, `goto` e operadores ternários.
*   Nomes de arquivos e funções seguem o padrão **snake_case**.

## 🤖 Relatório de Uso de IA
Como parte das exigências pedagógicas:
*   **Finalidade:** A IA foi utilizada para auxiliar na estruturação lógica de funções complexas (ex: `ft_split`, `ft_itoa`) e na revisão da conformidade com a Norma.
*   **Controle:** Todas as sugestões foram revisadas manualmente para garantir que padrões proibidos (como loops `for`) não fossem incluídos.
*   **Recursos:** Foram consultadas as `man pages` oficiais e o manual da Norma v4.1 fornecido pela escola.
