#include <stdio.h>

int main() {
    int v[5] = {5, 3, 4, 1, 2};
    int i, j, aux;

    for (i = 0; i < 5 - 1; i++) {
        for (j = 0; j < 5 - 1 - i; j++) {
            if (v[j] > v[j + 1]) {
                aux = v[j];
                v[j] = v[j + 1];
                v[j + 1] = aux;
            }
        }
    }

    printf("Numeros ordenados: ");

    for (i = 0; i < 5; i++) {
        printf("%d ", v[i]);
    }

    printf("\n");

    return 0;
}
