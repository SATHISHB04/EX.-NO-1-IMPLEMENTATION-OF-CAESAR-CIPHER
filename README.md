# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```

#include <stdio.h>
#include <string.h>
#include <ctype.h>

void caesar_cipher(char* text, int shift) {
    int i;
    char ch;

    for (i = 0; text[i] != '\0'; ++i) {
        ch = text[i];

        if (isupper(ch)) {
            text[i] = (ch + shift - 'A') % 26 + 'A';
        }
        else if (islower(ch)) {
            text[i] = (ch + shift - 'a') % 26 + 'a';
        }
    }
}

int main() {
    char text[100];
    int shift;

    printf("Name: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter shift amount: ");
    scanf("%d", &shift);

    caesar_cipher(text, shift);

    printf("Encrypted text: %s\n", text);

    return 0;
}
```
## OUTPUT:
<img width="1712" height="891" alt="Screenshot 2026-01-29 142255" src="https://github.com/user-attachments/assets/a1bdb95b-b304-4191-a373-b7e845124ddd" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
