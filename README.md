#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define MAX_NAME_LEN 100
#define MAX_ADDRESS_LEN 200
#define MAX_FILE_LEN 500
#define MAX_USER_DATA 100

// 01) Função que retorna o número de caracteres de um arquivo, ignorando espaços e quebras de linha
int contarCaracteres(const char *nome_arquivo) {
    FILE *arquivo = fopen(nome_arquivo, "r");
    if (!arquivo) {
        printf("Erro ao abrir o arquivo.\n");
        return -1;
    }
