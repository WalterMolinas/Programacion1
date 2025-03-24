#include <stdio.h>

int main() {
	int num, i, j, esPrimo;
	
	// Pedimos al usuario que ingrese un número
	printf("Ingresa un número: ");
	scanf("%d", &num);
	
	printf("Números primos entre 1 y %d:\n", num);
	
	for (i = 2; i <= num; i++) {
		esPrimo = 1; // Asumimos que el número es primo
		
		// Verificamos si el número es divisible por algún número menor a él
		for (j = 2; j <= i / 2; j++) {
			if (i % j == 0) {
				esPrimo = 0; // No es primo
			}
		}
		if (esPrimo == 1) {
			printf("%d ", i); // Mostramos el número si es primo
		}
	}
	return 0;
}
