## C++ Samples

### First one :

```
#include <iostream>
using namespace std;
struct student
{
    char name[50];
    int roll;
    float marks;
} s[10];
int main()
{
    cout << "Enter information of students: " << endl;
    // storing information
    for(int i = 0; i < 10; ++i)
    {
        s[i].roll = i+1;
        cout << "For roll number" << s[i].roll << "," << endl;
        cout << "Enter name: ";
        cin >> s[i].name;
        cout << "Enter marks: ";
        cin >> s[i].marks;
        cout << endl;
    }
    cout << "Displaying Information: " << endl;
    // Displaying information
    for(int i = 0; i < 10; ++i)
    {
        cout << "\nRoll number: " << i+1 << endl;
        cout << "Name: " << s[i].name << endl;
        cout << "Marks: " << s[i].marks << endl;
    }
    return 0;
}
```

### Second :

```
#include <iostream>
#include <cmath>
using namespace std;
long long convertDecimalToBinary(int);
int main()
{
    int n, binaryNumber;
    cout << "Enter a decimal number: ";
    cin >> n;
    binaryNumber = convertDecimalToBinary(n);
    cout << n << " in decimal = " << binaryNumber << " in binary" << endl ;
    return 0;
}
long long convertDecimalToBinary(int n)
{
    long long binaryNumber = 0;
    int remainder, i = 1, step = 1;
    while (n!=0)
    {
        remainder = n%2;
        cout << "Step " << step++ << ": " << n << "/2, Remainder = " << remainder << ", Quotient = " << n/2 << endl;
        n /= 2;
        binaryNumber += remainder*i;
        i *= 10;
    }
    return binaryNumber;
}
```