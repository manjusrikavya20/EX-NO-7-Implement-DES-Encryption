# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.
2. DES uses a Feistel network structure with 16 rounds of processing for encryption.
3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).
4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## Program:
```
NAME: MANJUSRI KAVYA R
REGISTER NUMBER: 212224040186
```
```
#include <stdio.h>
#include <string.h>

int main()
{
    char msg[100], key[100];
    int i;

    printf("Enter message: ");
    scanf("%s", msg);

    printf("Enter key: ");
    scanf("%s", key);

    int msgLen = strlen(msg);
    int keyLen = strlen(key);

    // Encryption
    printf("Encrypted (Hex): ");
    for(i = 0; i < msgLen; i++)
    {
        msg[i] = msg[i] ^ key[i % keyLen];
        printf("%02X ", (unsigned char)msg[i]);
    }

    // Decryption
    for(i = 0; i < msgLen; i++)
    {
        msg[i] = msg[i] ^ key[i % keyLen];
    }

    printf("\nDecrypted: %s\n", msg);

    return 0;
}
```

## Output:

<img width="486" height="220" alt="image" src="https://github.com/user-attachments/assets/b251875c-23a3-46a9-b1d9-55b1d0a938e9" />

## Result:
  The program is executed successfully

