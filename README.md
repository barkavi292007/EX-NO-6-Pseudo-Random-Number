# EX-NO-6-Pseudo-Random-Number

# AIM: 
Implementation of Pseudorandom Number Generation Using Standard library

# ALGORITHM:
Start the program and import the required libraries.
Seed the random number generator using the current time(i.e) rand(time(0));
Get the number of randon number to generate.
Pass the value for number of iterations and print the numbers.
End the program.

# PROGRAM:
```

#include <stdio.h>

int main()
{
    int i, seed, key, plain[100], cipher[100], decrypt[100];
    int n;

    printf("Enter seed value: ");
    scanf("%d", &seed);

    printf("Enter number of characters: ");
    scanf("%d", &n);

    printf("Enter plaintext values (ASCII): ");
    for(i = 0; i < n; i++)
        scanf("%d", &plain[i]);

    printf("\nPseudo Random Numbers: ");
    for(i = 0; i < n; i++)
    {
        seed = (seed * 7 + 3) % 100;
        printf("%d ", seed);

        cipher[i] = plain[i] ^ seed;
    }

    printf("\nEncrypted text: ");
    for(i = 0; i < n; i++)
        printf("%c", cipher[i]);

    seed = 10;  // Original seed value
    printf("\nDecrypted text: ");
    for(i = 0; i < n; i++)
    {
        seed = (seed * 7 + 3) % 100;
        decrypt[i] = cipher[i] ^ seed;
        printf("%c", decrypt[i]);
    }

    return 0;
}

```
# OUTPUT:
<img width="913" height="387" alt="image" src="https://github.com/user-attachments/assets/be9d57e2-f2a5-4928-85c8-3ae34bf175e2" />

# RESULT:
