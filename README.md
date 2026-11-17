include <iostream>
#include <cmath>
using namespace std;

// Function to calculate the roots
void roots(float a, float b, float c)
{
    float d, x1, x2;

    d = (b * b) - (4 * a * c);

    if (d > 0)
    {
        x1 = (-b + sqrt(d)) / (2 * a);
        x2 = (-b - sqrt(d)) / (2 * a);

        cout << "The roots are real and different." << endl;
        cout << "First root = " << x1 << endl;
        cout << "Second root = " << x2 << endl;
    }
    else if (d == 0)
    {
        x1 = -b / (2 * a);

        cout << "The roots are real and equal." << endl;
        cout << "Root = " << x1 << endl;
    }
    else
    {
        cout << "The roots are imaginary." << endl;
    }
}

int main()
{
    float a, b, c;

    cout << "Enter the value of a: ";
    cin >> a;

    cout << "Enter the value of b: ";
    cin >> b;

    cout << "Enter the value of c: ";
    cin >> c;

    if (a == 0)
    {
        cout << "This is not a quadratic equation.";
    }
    else
    {
        roots(a, b, c);
    }

    return 0;
}
