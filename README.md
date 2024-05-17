# Lista-1-N2

1. **Cadastro de Alunos:**
Crie uma estrutura `Aluno` com campos como nome, idade, matrícula, e média.
Em seguida, crie um programa que permita ao usuário cadastrar informações de
vários alunos e depois imprima essas informações na tela.

#include <stdio.h>

#define MAX_ALUNOS 100

// Definição da estrutura Aluno
typedef struct {
    char nome[50];
    int idade;
    int matricula;
    float media;
} Aluno;

int main() {
    Aluno alunos[MAX_ALUNOS];
    int numAlunos;

    // Pedir ao usuário o número de alunos a serem cadastrados
    printf("Digite o número de alunos a serem cadastrados: ");
    scanf("%d", &numAlunos);

    // Loop para cadastrar informações dos alunos
    for (int i = 0; i < numAlunos; i++) {
        printf("\nCadastro do Aluno %d:\n", i + 1);
        
        printf("Nome: ");
        scanf("%s", alunos[i].nome);

        printf("Idade: ");
        scanf("%d", &alunos[i].idade);

        printf("Matrícula: ");
        scanf("%d", &alunos[i].matricula);

        printf("Média: ");
        scanf("%f", &alunos[i].media);
    }

    // Imprimir informações dos alunos cadastrados
    printf("\nInformações dos Alunos Cadastrados:\n");
    for (int i = 0; i < numAlunos; i++) {
        printf("\nAluno %d:\n", i + 1);
        printf("Nome: %s\n", alunos[i].nome);
        printf("Idade: %d\n", alunos[i].idade);
        printf("Matrícula: %d\n", alunos[i].matricula);
        printf("Média: %.2f\n", alunos[i].media);
    }

    return 0;
}



2. **Cadastro de Produtos:**
Crie uma estrutura `Produto` com campos como nome, preço e quantidade em
estoque. Em seguida, permita ao usuário cadastrar vários produtos e depois
imprima essas informações na tela.

#include <stdio.h>

#define MAX_PRODUTOS 100
#define MAX_NOME 50

// Definição da estrutura Produto
typedef struct {
    char nome[MAX_NOME];
    float preco;
    int quantidade;
} Produto;

int main() {
    Produto produtos[MAX_PRODUTOS];
    int numProdutos;

    // Pedir ao usuário o número de produtos a serem cadastrados
    printf("Digite o número de produtos a serem cadastrados: ");
    scanf("%d", &numProdutos);
    getchar(); // Limpa o buffer de nova linha deixado pelo scanf

    // Loop para cadastrar informações dos produtos
    for (int i = 0; i < numProdutos; i++) {
        printf("\nCadastro do Produto %d:\n", i + 1);

        printf("Nome: ");
        fgets(produtos[i].nome, MAX_NOME, stdin);
        produtos[i].nome[strcspn(produtos[i].nome, "\n")] = 0; // Remove o caractere de nova linha

        printf("Preço: ");
        scanf("%f", &produtos[i].preco);
        getchar(); // Limpa o buffer de nova linha deixado pelo scanf

        printf("Quantidade em estoque: ");
        scanf("%d", &produtos[i].quantidade);
        getchar(); // Limpa o buffer de nova linha deixado pelo scanf
    }

    // Imprimir informações dos produtos cadastrados
    printf("\nInformações dos Produtos Cadastrados:\n");
    for (int i = 0; i < numProdutos; i++) {
        printf("\nProduto %d:\n", i + 1);
        printf("Nome: %s\n", produtos[i].nome);
        printf("Preço: %.2f\n", produtos[i].preco);
        printf("Quantidade em estoque: %d\n", produtos[i].quantidade);
    }

    return 0;
}




3. **Cadastro de Pessoas:**
Crie uma estrutura `Pessoa` com campos como nome, idade, e cidade. Permita ao
usuário cadastrar várias pessoas e depois imprima essas informações na tela.

#include <stdio.h>

#define MAX_PESSOAS 100
#define MAX_NOME 50
#define MAX_CIDADE 50

// Definição da estrutura Pessoa
typedef struct {
    char nome[MAX_NOME];
    int idade;
    char cidade[MAX_CIDADE];
} Pessoa;

int main() {
    Pessoa pessoas[MAX_PESSOAS];
    int numPessoas;

    // Pedir ao usuário o número de pessoas a serem cadastradas
    printf("Digite o número de pessoas a serem cadastradas: ");
    scanf("%d", &numPessoas);

    // Loop para cadastrar informações das pessoas
    for (int i = 0; i < numPessoas; i++) {
        printf("\nCadastro da Pessoa %d:\n", i + 1);

        printf("Nome: ");
        scanf("%s", pessoas[i].nome);

        printf("Idade: ");
        scanf("%d", &pessoas[i].idade);

        printf("Cidade: ");
        scanf("%s", pessoas[i].cidade);
    }

    // Imprimir informações das pessoas cadastradas
    printf("\nInformações das Pessoas Cadastradas:\n");
    for (int i = 0; i < numPessoas; i++) {
        printf("\nPessoa %d:\n", i + 1);
        printf("Nome: %s\n", pessoas[i].nome);
        printf("Idade: %d\n", pessoas[i].idade);
        printf("Cidade: %s\n", pessoas[i].cidade);
    }

    return 0;
}




4. **Registro de Funcionários:**
Crie uma estrutura `Funcionario` com campos como nome, cargo e salário.
Permita ao usuário cadastrar informações de vários funcionários e depois imprima
essas informações na tela.

#include <stdio.h>

#define MAX_FUNCIONARIOS 100
#define MAX_NOME 50
#define MAX_CARGO 50

// Definição da estrutura Funcionario
typedef struct {
    char nome[MAX_NOME];
    char cargo[MAX_CARGO];
    float salario;
} Funcionario;

int main() {
    Funcionario funcionarios[MAX_FUNCIONARIOS];
    int numFuncionarios;

    // Pedir ao usuário o número de funcionários a serem cadastrados
    printf("Digite o número de funcionários a serem cadastrados: ");
    scanf("%d", &numFuncionarios);

    // Loop para cadastrar informações dos funcionários
    for (int i = 0; i < numFuncionarios; i++) {
        printf("\nCadastro do Funcionário %d:\n", i + 1);

        printf("Nome: ");
        scanf("%s", funcionarios[i].nome);

        printf("Cargo: ");
        scanf("%s", funcionarios[i].cargo);

        printf("Salário: ");
        scanf("%f", &funcionarios[i].salario);
    }

    // Imprimir informações dos funcionários cadastrados
    printf("\nInformações dos Funcionários Cadastrados:\n");
    for (int i = 0; i < numFuncionarios; i++) {
        printf("\nFuncionário %d:\n", i + 1);
        printf("Nome: %s\n", funcionarios[i].nome);
        printf("Cargo: %s\n", funcionarios[i].cargo);
        printf("Salário: %.2f\n", funcionarios[i].salario);
    }

    return 0;
}




5. **Cadastro de Livros:**
Crie uma estrutura `Livro` com campos como título, autor e ano de publicação.
Permita ao usuário cadastrar vários livros e depois imprima essas informações na
tela.

#include <stdio.h>

#define MAX_LIVROS 100
#define MAX_TITULO 100
#define MAX_AUTOR 50

// Definição da estrutura Livro
typedef struct {
    char titulo[MAX_TITULO];
    char autor[MAX_AUTOR];
    int anoPublicacao;
} Livro;

int main() {
    Livro livros[MAX_LIVROS];
    int numLivros;

    // Pedir ao usuário o número de livros a serem cadastrados
    printf("Digite o número de livros a serem cadastrados: ");
    scanf("%d", &numLivros);

    // Loop para cadastrar informações dos livros
    for (int i = 0; i < numLivros; i++) {
        printf("\nCadastro do Livro %d:\n", i + 1);

        printf("Título: ");
        scanf("%s", livros[i].titulo);

        printf("Autor: ");
        scanf("%s", livros[i].autor);

        printf("Ano de Publicação: ");
        scanf("%d", &livros[i].anoPublicacao);
    }

    // Imprimir informações dos livros cadastrados
    printf("\nInformações dos Livros Cadastrados:\n");
    for (int i = 0; i < numLivros; i++) {
        printf("\nLivro %d:\n", i + 1);
        printf("Título: %s\n", livros[i].titulo);
        printf("Autor: %s\n", livros[i].autor);
        printf("Ano de Publicação: %d\n", livros[i].anoPublicacao);
    }

    return 0;
}
