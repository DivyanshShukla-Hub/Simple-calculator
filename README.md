# Simple-calculator

 
 # 1 In C programming language    
 
 
 
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

 How It Works
  
 1 Get User Input: The input() function prompts the user for information and reads what they type as a string (text).

 2 Error Handling: The entire logic is wrapped in a try...except block. The program tries to run the code inside. If the user enters text where a number is expected, a ValueError occurs, and the        program jumps to the except ValueError: block and prints a friendly error message instead of crashing.

 3 Convert Text to Numbers: The float() function converts the user's string input into a floating-point number (a number that can have decimals), so we can perform mathematical operations on it.

 4 Conditional Logic: An if-elif-else chain checks which operator the user entered. Based on the operator, it runs the appropriate calculation.

 5 Division by Zero: The code includes a special check if num2 == 0: before performing division to prevent a ZeroDivisionError, which would crash the program.

 6 Print the Result: The program uses an f-string (the f"..." syntax) to easily format and print the final result in a readable way.

 

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


 


# In c+

 
How it works:

1. It asks the user to enter an operator (+, -, *, /).

2. Then it takes two numbers as input.

3. It uses a switch-case statement to perform the correct operation.

4. It checks for division by zero when the operator is /. 

  
        #include <iostream>
        using namespace std;

        int main() {
        char op;
        double num1, num2;

    
         cout << "Enter operator (+, -, *, /): ";
         cin >> op;

         cout << "Enter two numbers: ";
        cin >> num1 >> num2;

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




  # In C++


   How it works:
 1. User enters an operator (+ - * /).
 2. Then inputs two numbers.
 3. switch checks which operation to perform.
 4. Division checks for 0 to avoid errors. 


        #include <iostream>
        using namespace std;

        int main() {
        char op;
        float num1, num2;

        cout << "Enter operator (+, -, *, /): ";
        cin >> op;

        cout << "Enter two numbers: ";
        cin >> num1 >> num2;

        switch (op) {
        case '+':
            cout << "Result: " << num1 + num2;
            break;
        case '-':
            cout << "Result: " << num1 - num2;
            break;
        case '*':
            cout << "Result: " << num1 * num2;
            break;
        case '/':
            if (num2 != 0)
                cout << "Result: " << num1 / num2;
            else
                cout << "Error! Division by zero.";
            break;
        default:
            cout << "Invalid operator!";
            break;
          }

        return 0;
        }

  # In  C+++

How it works:

1.The program asks the user to enter an operator (+, -, *, /, %, ^) or q to quit.
2.It takes two numbers as input.
3.Based on the operator, it performs the correct calculation.
4.It displays the result.
5.It checks for invalid inputs (like letters or dividing by zero).
6.The loop repeats until the user enters q to exit.

 // simple_calculator.cpp
 
     #include <iostream>
     #include <cmath>    // for pow
     #include <limits>   // for numeric_limits

    using namespace std;

    void clearInput() {
    cin.clear();
    cin.ignore(numeric_limits<streamsize>::max(), '\n');
    }

    int main() {
    cout << "Simple Calculator (C++)\n";
    cout << "Supported operations: +  -  *  /  %  ^ (power)\n\n";

    while (true) {
        cout << "Enter operation (+ - * / % ^) or q to quit: ";
        char op;
        if (!(cin >> op)) {
            clearInput();
            cout << "Invalid input. Try again.\n";
            continue;
        }
        if (op == 'q' || op == 'Q') {
            cout << "Goodbye!\n";
            break;
        }

        if (op == '%') {
            long long a, b;
            cout << "Enter two integers (a b): ";
            if (!(cin >> a >> b)) {
                clearInput();
                cout << "Invalid integer input. Try again.\n";
                continue;
            }
            if (b == 0) {
                cout << "Error: Division by zero (modulus undefined).\n";
                continue;
            }
            cout << a << " % " << b << " = " << (a % b) << "\n\n";
        } else if (op == '+' || op == '-' || op == '*' || op == '/' || op == '^') {
            double x, y;
            cout << "Enter two numbers (a b): ";
            if (!(cin >> x >> y)) {
                clearInput();
                cout << "Invalid number input. Try again.\n";
                continue;
            }
            if (op == '+') {
                cout << x << " + " << y << " = " << (x + y) << "\n\n";
            } else if (op == '-') {
                cout << x << " - " << y << " = " << (x - y) << "\n\n";
            } else if (op == '*') {
                cout << x << " * " << y << " = " << (x * y) << "\n\n";
            } else if (op == '/') {
                if (y == 0.0) {
                    cout << "Error: Division by zero.\n\n";
                } else {
                    cout << x << " / " << y << " = " << (x / y) << "\n\n";
                }
            } else { // power
                cout << x << " ^ " << y << " = " << pow(x, y) << "\n\n";
            }
        } else {
            cout << "Unknown operation '" << op << "'. Try again.\n";
        }
    }

    return 0;
    }


  # In Java

  How it works:

 1.It takes two numbers as input from the user.
2. You choose an operator (+, -, *, /).
3.It performs the calculation using a switch statement.
4.It prints the result on the screen.




        import java.util.Scanner;

        public class SimpleCalculator {
        public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double num1, num2;
        char operator;

        System.out.println("Enter first number: ");
        num1 = input.nextDouble();

        System.out.println("Enter operator (+, -, *, /): ");
        operator = input.next().charAt(0);

        System.out.println("Enter second number: ");
        num2 = input.nextDouble();

        double result = 0;

        switch (operator) {
            case '+':
                result = num1 + num2;
                break;

            case '-':
                result = num1 - num2;
                break;

            case '*':
                result = num1 * num2;
                break;

            case '/':
                if (num2 != 0)
                    result = num1 / num2;
                else {
                    System.out.println("Error! Division by zero is not allowed.");
                    return;
                }
                break;

            default:
                System.out.println("Invalid operator!");
                return;
        }

        System.out.println("Result: " + result);
        input.close();
    }
    }


