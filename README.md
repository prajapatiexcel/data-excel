#include <stdio.h>
int main()
{
    int num1, num2;
    char operation;

    printf("पहला नंबर दर्ज करें: ");
    scanf("%d", &num1);

    printf("दूसरा नंबर दर्ज करें: ");
    scanf("%d", &num2);

    printf("ऑपरेशन चुनें (+, -, *, /): ");
    scanf(" %c", &operation);

    switch (operation) {
        case '+':
            printf("%d + %d = %d\n", num1, num2, num1 + num2);
            break;
        case '-':
            printf("%d - %d = %d\n", num1, num2, num1 - num2);
            break;
        case '*':
            printf("%d * %d = %d\n", num1, num2, num1 * num2);
            break;
        case '/':
            if (num2 != 0) {
                printf("%d / %d = %d\n", num1, num2, num1 / num2);
            } else {
                printf("शून्य से विभाजन नहीं किया जा सकता है\n");
            }
            break;
        default:
            printf("अवैध ऑपरेशन\n");
            break;
    }

    return 0;
}
