# M-todo-burbuja-
#include <stdio.h>

void intercambiar(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

void ordenamientoBurbuja(int arr[], int n) {
    for (int i = 0; i < n-1; i++) {
        for (int j = 0; j < n-i-1; j++) {
            if (arr[j] > arr[j+1]) {
                intercambiar(&arr[j], &arr[j+1]);
            }
        }
    }
}

void mostrarArreglo(int arr[], int size) {
    for (int i=0; i < size; i++)
        printf("%d ", arr[i]);
    printf("\n");
}

int main() {
    int arreglo[] = {64, 25, 12, 22, 11};
    int n = sizeof(arreglo)/sizeof(arreglo[0]);

    printf("Arreglo original: ");
    mostrarArreglo(arreglo, n);

    ordenamientoBurbuja(arreglo, n);

    printf("Arreglo ordenado: ");
    mostrarArreglo(arreglo, n);

    return 0;
}
