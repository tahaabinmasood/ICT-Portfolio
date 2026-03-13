# Assignment-1
#include <iostream>
#include <stdexcept>

using namespace std;

int divide(int a, int b) {
    if (b == 0) {
        throw runtime_error("Bug detected: Division by zero!");
    }
    return a / b;
}

int main() {
    int x, y;

    cout << "Enter two numbers: ";
    cin >> x >> y;

    try {
        int result = divide(x, y);
        cout << "Result: " << result << endl;
    }
    catch (exception &e) {
        cerr << "Error: " << e.what() << endl;
        cerr << "Fix your input or check the code." << endl;
    }

    return 0;
}