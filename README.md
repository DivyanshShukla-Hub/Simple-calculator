# Simple-calculator
# Simple Command-Line Calculator in C

This is a simple calculator built using the C programming language. It's a beginner-friendly project created to practice fundamental C concepts like variables, user input/output (`scanf`/`printf`), and control flow (`switch` statement).

This project was completed as part of my learning journey into C programming.

## Features ✨

* Performs basic arithmetic operations: Addition (+), Subtraction (-), Multiplication (*), and Division (/).
* Accepts decimal numbers (`double` data type).
* Includes basic error handling for division by zero and invalid operators.
* Runs in any standard command-line terminal.



  #include <stdio.h>

int main() {
    // Variable to store the operator (+, -, *, /)
    char operator;
    
    // Variables to store the two numbers
    double num1, num2;

    // Ask the user to enter an operator
    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator); // Note the space before %c

    // Ask the user to enter two numbers
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    // The switch statement checks which operator was entered
    switch (operator) {
        case '+':
            printf("%.1lf + %.1lf = %.1lf\n", num1, num2, num1 + num2);
            break;
        
        case '-':
            printf("%.1lf - %.1lf = %.1lf\n", num1, num2, num1 - num2);
            break;
        
        case '*':
            printf("%.1lf * %.1lf = %.1lf\n", num1, num2, num1 * num2);
            break;
        
        case '/':
            // Check if the second number is zero before dividing
            if (num2 != 0.0) {
                printf("%.1lf / %.1lf = %.1lf\n", num1, num2, num1 / num2);
            } else {
                printf("Error! Division by zero is not allowed.\n");
            }
            break;

        // If the operator is not +, -, *, or /, show an error
        default:
            printf("Error! Operator is not correct.\n");
    }

    return 0;
    }
 THANK YOU FOR GIVING YOOUR  TIME
