# Simple-calculator

 
 # 1 In C programming language    \
 


This is a simple calculator built using the C programming language. It's a beginner-friendly project created to practice fundamental C concepts like variables, user input/output (`scanf`/`printf`), and control flow (`switch` statement).

This project was completed as part of my learning journey into C programming.
 
## Features :  

* Performs basic arithmetic operations: Addition (+), Subtraction (-), Multiplication (*), and Division (/).
 * Accepts decimal numbers (`double` data type).
 * Includes basic error handling for division by zero and invalid operators.
 * Runs in any standard command-line terminal.
 
 

       #include <stdio.h>

       int main() {
    
       char operator;

       printf("Enter an operator (+, -, *, /): ");
       scanf(" %c", &operator); // Note the space before %c

    
       printf("Enter two numbers: ");
       scanf("%lf %lf", &num1, &num2);

   
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
           
            if (num2 != 0.0) {
                printf("%.1lf / %.1lf = %.1lf\n", num1, num2, num1 / num2);
            } else {
                printf("Error! Division by zero is not allowed.\n");
            }
            break;

      
        default:
            printf("Error! Operator is not correct.\n");
       }

       return 0;
         }

   # 2 In Phyton 

  calculator.py

    print("--- Simple Python Calculator ---")

  
    num1 = float(input("Enter the first number: "))
    operator = input("Enter an operator (+, -, *, /): ")
    num2 = float(input("Enter the second number: "))

    if operator == '+':
        result = num1 + num2
        print(f"The result is: {num1} + {num2} = {result}")

    elif operator == '-':
        result = num1 - num2
        print(f"The result is: {num1} - {num2} = {result}")

    elif operator == '*':
        result = num1 * num2
        print(f"The result is: {num1} * {num2} = {result}")

    elif operator == '/':
        if num2 == 0:
            print("Error: Division by zero is not allowed.")
        else:
            result = num1 / num2
            print(f"The result is: {num1} / {num2} = {result}")
    
    else:
        print("Error: Invalid operator. Please use +, -, *, or /.")

    except ValueError:
      print("Error: Invalid input. Please enter valid numbers.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")


  How It Works
  
 1 Get User Input: The input() function prompts the user for information and reads what they type as a string (text).

 2 Error Handling: The entire logic is wrapped in a try...except block. The program tries to run the code inside. If the user enters text where a number is expected, a ValueError occurs, and the        program jumps to the except ValueError: block and prints a friendly error message instead of crashing.

 3 Convert Text to Numbers: The float() function converts the user's string input into a floating-point number (a number that can have decimals), so we can perform mathematical operations on it.

 4 Conditional Logic: An if-elif-else chain checks which operator the user entered. Based on the operator, it runs the appropriate calculation.

 5 Division by Zero: The code includes a special check if num2 == 0: before performing division to prevent a ZeroDivisionError, which would crash the program.

 6 Print the Result: The program uses an f-string (the f"..." syntax) to easily format and print the final result in a readable way.



# In c+

  
    #include <iostream>
    using namespace std;

    int main() {
    char op;
    double num1, num2;

    // Asking user for input
    cout << "Enter operator (+, -, *, /): ";
    cin >> op;

    cout << "Enter two numbers: ";
    cin >> num1 >> num2;

    // Perform calculation based on operator
    switch(op) {
        case '+':
            cout << "Result: " << num1 + num2 << endl;
            break;

        case '-':
            cout << "Result: " << num1 - num2 << endl;
            break;

        case '*':
            cout << "Result: " << num1 * num2 << endl;
            break;

        case '/':
            if (num2 != 0)
                cout << "Result: " << num1 / num2 << endl;
            else
                cout << "Error! Division by zero is not allowed." << endl;
            break;

        default:
            cout << "Invalid operator!" << endl;
            break;
    }

    return 0;
     }

How it works:

1. It asks the user to enter an operator (+, -, *, /).

2. Then it takes two numbers as input.

3. It uses a switch-case statement to perform the correct operation.

4. It checks for division by zero when the operator is /.
