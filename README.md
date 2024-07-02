# lecture--14-cipher-school
In this lecture i had learned about functions PART-2 about how to call multiple functions and hoe to create multiple functions and aslo about void function does not return any type expect void her aslo 
learned about an example of how to create the multiple functions with 2 to 3 modules and here is the example of the how it works here is the basic example using switch case 
#include <iostream>
using namespace std;


int add(int a, int b);
int subtract(int a, int b);
int multiply(int a, int b);
double divide(int a, int b);

int main() {
    int num1, num2;
    char operation;

    
    cout << "Enter first number: ";
    cin >> num1;
    cout << "Enter second number: ";
    cin >> num2;
    cout << "Choose an operation (+, -, *, /): ";
    cin >> operation;

   
    switch (operation) {
        case '+':
            cout << "Result: " << add(num1, num2) << endl;
            break;
        case '-':
            cout << "Result: " << subtract(num1, num2) << endl;
            break;
        case '*':
            cout << "Result: " << multiply(num1, num2) << endl;
            break;
        case '/':
            
            if (num2 != 0) {
                cout << "Result: " << divide(num1, num2) << endl;
            } else {
                cout << "Error: Division by zero!" << endl;
            }
            break;
        default:
            cout << "Invalid operation!" << endl;
            break;
    }

    return 0;
}


int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}

int multiply(int a, int b) {
    return a * b;
}

double divide(int a, int b) {
    return static_cast<double>(a) / b;
}
