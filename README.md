# Mini-Calculator.
#include <iostream>  // Author: Muhammad Bilal
using namespace std;

int main() {
    float num1, num2;
    char symbol;
    char choice;

    do {
        // Input
        cout << "\n===== Mini Calculator =====" << endl;
        cout << "Enter first number: ";
        cin >> num1;
        cout << "Enter operator (+, -, *, /): ";
        cin >> symbol;
        cout << "Enter second number: ";
        cin >> num2;

        // Processing
        switch (symbol) {
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
                if (num2 == 0) {
                    cout << "Error: Division by zero is undefined!" << endl;
                } else {
                    cout << "Result: " << num1 / num2 << endl;
                }
                break;
            default:
                cout << "Syntax Error: Invalid operator entered." << endl;
        }

        // Option to Continue or Exit
        cout << "Do you want to perform another calculation? (yes/no): ";
        cin >> choice;

    } while (choice == 'y' || choice == 'Y');

    cout << "Thank you for using the calculator!" << endl;
    return 0;
}
