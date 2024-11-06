#include <stdio.h>
#include <math.h>
#include<stdbool.h>

bool is_prime(int num)
 {
    if (num <= 1) {
        return false;
    }
    for (int i = 2; i <= sqrt(num); ++i) {
        if (num % i == 0) {
            return false;
        }
    }
    return true;
}
int fibonacci(int num)
 {
    if (num == 0 || num == 1) {
        return num;
    } else {
        return fibonacci(num - 1) + fibonacci(num - 2);
    }
}
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
