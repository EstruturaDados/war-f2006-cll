#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define NUM_TERRITORIOS 5

// Define a estrutura do território
typedef struct {
    char nome[30];
    char cor[10];
    int tropas;
} Territorio;

// Remove o '\n' do final de strings lidas com fgets
void limparNovaLinha(char* str) {
    size_t len = strlen(str);
    if (len > 0 && str[len - 1] == '\n') {
        str[len - 1] = '\0';
    }
}

// Função para cadastrar os dados dos territórios
void cadastrarTerritorios(Territorio territorios[], int tamanho) {
    printf("🔰 Cadastro dos Territórios:\n");

    for (int i = 0; i < tamanho; i++) {
        printf("\n📍 Território %d:\n", i + 1);

        printf("Nome: ");
        fgets(territorios[i].nome, sizeof(territorios[i].nome), stdin);
        limparNovaLinha(territorios[i].nome);

        printf("Cor do Exército: ");
        fgets(territorios[i].cor, sizeof(territorios[i].cor), stdin);
        limparNovaLinha(territorios[i].cor);

        printf("Número de Tropas: ");
        scanf("%d", &territorios[i].tropas);
        getchar();  // Limpa o '\n' deixado pelo scanf
    }
}

// Função para exibir os territórios cadastrados
void exibirTerritorios(const Territorio territorios[], int tamanho) {
    printf("\n🌍 Estado Atual do Mapa:\n");

    for (int i = 0; i < tamanho; i++) {
        printf("\n=========================\n");
        printf("🏷️  Nome: %s\n", territorios[i].nome);
        printf("🎨 Cor do Exército: %s\n", territorios[i].cor);
        printf("🪖 Tropas: %d\n", territorios[i].tropas);
    }

    printf("\n=========================\n");
}

int main() {
    Territorio territorios[NUM_TERRITORIOS];

    cadastrarTerritorios(territorios, NUM_TERRITORIOS);
    exibirTerritorios(territorios, NUM_TERRITORIOS);

    return 0;
}
