#include <stdio.h>
#include <math.h>
#include<stdbool.h>
int main()
 {
    int terms;
    printf("Enter a positive integer: ");
    scanf("%d", &terms);

    if (is_prime(terms)) {
        printf("%d is a prime number.\n", terms);
    } else {
        printf("%d is not a prime number.\n", terms);
    }
printf("\n");
  

    for (int n = 0; n < terms; ++n) {
        printf("%d ", fibonacci(n));
    }
}
