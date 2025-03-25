#include <stdio.h>

int main() {
	int num, i, cont, primo;
	
	printf("Ingresa un número: ");
	scanf("%d", &num);
	
	printf("Números primos entre 1 y %d:\n", num);
	
	for (i = 2; i <= num; i++) {
		primo = 1;
  
		for (cont = 2; cont <= i / 2; cont++) {
			if (i % cont == 0) {
				primo = 0;
			}
		}
		if (primo == 1) {
			printf("%d ", i);
		}
	}
	return 0;
}
