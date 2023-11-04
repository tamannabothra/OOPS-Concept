# OOPS-Concept
Object-oriented programming aims to implement real-world entities like inheritance, hiding, polymorphism, etc. in programming. The main aim of OOP is to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.
There are some basic concepts that act as the building blocks of OOPs i.e.
<li>	Class</li>
<li>	Objects</li>
<li>	Encapsulation</li>
<li>	Abstraction</li>
<li>	Polymorphism</li>
<li>	Inheritance</li>
<li>	Dynamic Binding</li>
<li>Message Passing</li>

# Classes and Objects

It is a user-defined data type, which holds its own data members and member functions, which can be accessed and used by creating an instance of that class. A class is like a blueprint for an object.<br/>
In C++, Object is a real world entity, for example, chair, car, pen, mobile, laptop etc. In other words, object is an entity that has state and behavior. Here, state means data and behavior means functionality. Object is a runtime entity, it is created at runtime.

# Encapsulation
```
#include <iostream>
using namespace std;
class Rectangle {
  public
    int length;
    int breadth;
    Rectangle(int len, int brth) : length(len), breadth(brth) {}
    int getArea() {
      return length * breadth;
    }
};
int main() { 
  Rectangle rect(8, 6);
  cout << "Area = " << rect.getArea();

  return 0;
}
```
# Abstraction
```
#include <iostream>
using namespace std;
 
class implementAbstraction {
private:
    int a, b;
 
public:
    void set(int x, int y)
    {
        a = x;
        b = y;
    }
 
    void display()
    {
        cout << "a = " << a << endl;
        cout << "b = " << b << endl;
    }
};
 
int main()
{
    implementAbstraction obj;
    obj.set(10, 20);
    obj.display();
    return 0;
}
```

# Polymorphism
```
#include <bits/stdc++.h>
 
using namespace std;
class Value {
public:

    void func(int x)
    {
        cout << "value of x is " << x << endl;
    }
    void func(double x)
    {
        cout << "value of x is " << x << endl;
    }

    void func(int x, int y)
    {
        cout << "value of x and y is " << x << ", " << y
             << endl;
    }
};

int main()
{
    Value obj1;
    obj1.func(7);
    obj1.func(9.132);
    obj1.func(85, 64);
    return 0;
}
```
# Inheritance
```
class Vehicle {
  public:
    string brand = "Ford";
    void honk() {
      cout << "Tuut, tuut! \n" ;
    }
};
class Car: public Vehicle {
  public:
    string model = "Mustang";
};
int main() {
  Car myCar;
  myCar.honk();
  cout << myCar.brand + " " + myCar.model;
  return 0;
}

```
# Dynamic Binding
```
#include <iostream>
using namespace std;
class Trial {
public:
    void call_Function() 
    {
        print();
    }
    void print() 
    {
        cout << "Printing the Base class Content" << endl;
    }
};
class Trial2 : public Trial 
{
public:
    void print() 
    {
        cout << "Printing the Derived class Content"
             << endl;
    }
};
int main()
{
    Trial try; 
    try.call_Function(); 
    Trial2 try2; 
    try.call_Function();                                
    return 0;
}
```
# Message Passing

Objects communicate with one another by sending and receiving information. A message for an object is a request for the execution of a procedure and therefore will invoke a function in the receiving object that generates the desired results. Message passing involves specifying the name of the object, the name of the function, and the information to be sent.

