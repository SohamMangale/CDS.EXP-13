# EXPERIMENT - 13
## Aim
To study and implement Constructor Overloading

## Apparatus
Vs Code

## Theory
### Constructor Overloading :
Constructor overloading in C++ is a concept where a class can have more than one constructor, each having a different set of parameters. This allows creating objects in various ways, offering flexibility in how an object is initialized. The appropriate constructor is invoked based on the arguments passed when an object is created.

### Key Concepts about constructor overloading :
Multiple Constructors: In constructor overloading, each constructor has a unique signature determined by the number and types of parameters. This lets developers initialize objects in different ways depending on the situation.

### No Return Type: 
Constructors do not have a return type (not even void), as their primary function is to initialize an object. Once the constructor is called, the object gets initialized.

### Default Constructor: 
A constructor without parameters, known as the default constructor, initializes an object with default values. If no constructors are defined in a class, the compiler provides a default constructor.

### Parameterized Constructor: 
This constructor accepts parameters, allowing the object to be initialized with specific values during creation.

### Copy Constructor: 
A copy constructor takes a reference to another object of the same class and creates a new object as a copy of the existing one.

## Codes :
### 1.
~~~
//soham
//entc B1
//23070123084
//experiment 13
#include <iostream>
using namespace std;

class Room {
private:
    double length;
    double breadth;

public:
    
    Room() {
        length = 9;
        breadth = 7;
    }

    
    Room(double l, double b) {
        length = l;
        breadth = b;
    }

    
    Room(double len) {
        length = len;
        breadth = 8.1;
    }

    double calculateArea() {
        return length * breadth;
    }
};

int main() {
    Room r1;
    Room r2(8.6, 6.9);
    Room r3(9, 9);
       
    cout << "Area of r1: " << r1.calculateArea() << endl;
    cout << "Area of r2: " << r2.calculateArea() << endl;
    cout << "Area of r3: " << r3.calculateArea() << endl;

    return 0;
}
~~~
### 2.
~~~
//soham
//entc B1
//23070123084
//experiment 13A
#include <iostream>
using namespace std;

class fetch {
    int num;
public:
   
    fetch() {
        num = 45;
        cout << num << " 1st" << endl;
    }

   
    fetch(int x) {
        num = x;
        cout << num << " 2nd" << endl;
    }

   
    fetch(const fetch &b) {
        num = b.num;
        cout << num << " copy" << endl;
    }

    
    void disp() const {
        cout << num << endl;
    }
};

int main() {
    fetch f1;     
    fetch f2(25); 
    fetch f3(f1); 

   
    f1.disp();
    f2.disp();
    f3.disp();

    return 0;
}
~~~
## Outputs :
### 1.
![image](https://github.com/user-attachments/assets/feb638a6-ff26-4d17-b278-2024c6644302)


### 2.
![image](https://github.com/user-attachments/assets/b76a188e-c492-422f-8aae-47c2f8a0d647)


## Conclusion :
Constructor overloading is a powerful feature in C++ that enhances code flexibility, making it easier to manage how objects are created.
Proper use of overloaded constructors helps improve code clarity and efficiency
