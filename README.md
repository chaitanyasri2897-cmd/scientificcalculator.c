# scientificcalculator.c

#include <stdio.h>
#include <math.h>

int main() {
    int choice;
    double num1, num2, result;

    do {
      
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Square Root\n");
        printf("6. Power (x^y)\n");
        printf("7. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch(choice) {

            case 1:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = num1 + num2;
                printf("Result = %.2lf\n", result);
                break;

            case 2:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = num1 - num2;
                printf("Result = %.2lf\n", result);
                break;

            case 3:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &num1, &num2);
                result = num1 * num2;
                printf("Result = %.2lf\n", result);
                break;

            case 4:
                printf("Enter dividend and divisor: ");
                scanf("%lf %lf", &num1, &num2);
                if(num2 == 0)
                    printf("Error! Division by zero.\n");
                else {
                    result = num1 / num2;
                    printf("Result = %.2lf\n", result);
                }
                break;

            case 5:
                printf("Enter a number: ");
                scanf("%lf", &num1);
                if(num1 < 0)
                    printf("Error! Square root of negative number.\n");
                else {
                    result = sqrt(num1);
                    printf("Square Root = %.2lf\n", result);
                }
                break;

            case 6:
                printf("Enter base and exponent: ");
                scanf("%lf %lf", &num1, &num2);
                result = pow(num1, num2);
                printf("Result = %.2lf\n", result);
                break;

            case 7:
                printf("Exiting calculator\n");
                break;

            default:
                printf("Invalid choice! Please try again.\n");
        }

    } while(choice != 7);

    return 0;
}



    <img width="1100" height="793" alt="image" src="https://github.com/user-attachments/assets/8ecc73cf-6119-47ef-b728-1b1396ba0bb8" />
