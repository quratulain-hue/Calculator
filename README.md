#include <iostream>
using namespace std;

class Calculator {
private:
    double num1, num2, result;
    char op;
    
public:
    void getInput() {
        cout << "Enter first number: ";
        cin >> num1;
        
        cout << "Enter operator (+, -, *, /): ";
        cin >> op;
        
        cout << "Enter second number: ";
        cin >> num2;
    }
    
    void calculate() {
        if (op == '+') {
            result = num1 + num2;
            displayResult();
        }
        else if (op == '-') {
            result = num1 - num2;
            displayResult();
        }
        else if (op == '*') {
            result = num1 * num2;
            displayResult();
        }
        else if (op == '/') {
            if (num2 != 0) {
                result = num1 / num2;
                displayResult();
            } else {
                cout << "Error: Cannot divide by zero" << endl;
            }
        }
        else {
            cout << "Invalid operator" << endl;
        }
    }
    
    void displayResult() {
        cout << "Result: " << result << endl;
    }
};

int main() {
    Calculator calc;
    
    calc.getInput();
    calc.calculate();
    
    return 0;
}

