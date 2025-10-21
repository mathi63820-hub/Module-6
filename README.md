# 🐍 Python OOP: Abstract Class & Method Example
## 🎯 AIM
To create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle.

## 🧠 ALGORITHM
Import ABC module:

Use from abc import ABC, abstractmethod to define abstract classes and methods. Create Abstract Class Shape:

Define an abstract method calculate_area() with @abstractmethod. Create Subclass Rectangle:

Set default values for length and breadth. Override calculate_area() to compute the rectangle area. Create Subclass Circle:

Set default value for radius. Override calculate_area() to compute the circle area. Create Objects & Call Methods:

Instantiate Rectangle and Circle. Call their calculate_area() methods.

## 💻 Program
```
from abc import ABC, abstractmethod
import math
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self, length=5, breadth=3):
        self.length = length
        self.breadth = breadth
    def calculate_area(self):
        return self.length * self.breadth
class Circle(Shape):
    def __init__(self, radius=4):
        self.radius = radius
    def calculate_area(self):
        return math.pi * (self.radius ** 2)
rect = Rectangle()
circle = Circle()
print("Rectangle area:", rect.calculate_area())
print("Circle area:", circle.calculate_area())
```
## Output
<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/020d06d0-dcb0-4e41-929d-dc44fb3b7a06" />

## Result
Thus To create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle has been executed sucessfully.

# 🐍 Python OOP: Encapsulation with Private Members
## 🎯 AIM
To implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth.

## 🧠 ALGORITHM
Define the Class:

Create a class Rectangle with two private attributes: __length and __breadth. Initialize Variables:

Use the init() constructor to set initial values for __length and __breadth. Print Values:

Display the private variables from within the class to demonstrate access. Instantiate the Object:

Create an object of the Rectangle class to trigger the constructor.

## 💻 Program
```
class Rectangle:
    def __init__(self, length, breadth):
        # Private member variables
        self.__length = length
        self.__breadth = breadth

    def display(self):
        # Accessing private variables within the class
        print(f"Length: {self.__length}")
        print(f"Breadth: {self.__breadth}")
Create an object of Rectangle
rect = Rectangle(10, 5)
rect.display()
```
## Output
<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/3e8d185d-e1b5-4123-b910-86e06ad24212" />

## Result
Thus To implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth has been executed sucessfully.

# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python
## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method.

## 📋 ALGORITHM:
Define the Fish class with a method named type() that prints "fish". Define the Shark class as a subclass of Fish, and override the type() method to print "shark". Create an instance of the Fish class named obj_goldfish. Create an instance of the Shark class named obj_hammerhead. Use a for loop to iterate over both objects. Within the loop, call the type() method using the loop variable. Output will demonstrate method overriding: printing "fish" and "shark" accordingly.

## 💻 PROGRAM:
```
class Fish:
    def type(self):
        print("fish")
class Shark(Fish):
    def type(self):
        print("shark")
obj_goldfish = Fish()
obj_hammerhead = Shark()
for obj in (obj_goldfish, obj_hammerhead):
    obj.type()
```
## OUTPUT
<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/49efbcae-db34-44cf-9c5a-5cca20258b7b" />

## RESULT
Thus To write a Python program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method has been executed sucessfully.

# 🐍 Python OOP: Operator Overloading (Less Than <)
## 🎯 AIM
To write a Python program that demonstrates operator overloading by overloading the less than (<) operator using a custom class.

## 🧠 ALGORITHM
Create Class A:

Define the init() method to initialize the object with a value a. Overload the < Operator:

Define the lt() method with logic: If self.a < o.a, return "ob1 is less than ob2" Else, return "ob2 is less than ob1" Create Objects:

Instantiate two objects ob1 and ob2 with values. Use < Operator:

Use print(ob1 < ob2) to trigger the overloaded behavior.

## 💻 Program
```
class A:
    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"
ob1 = A(10)
ob2 = A(20)
print(ob1 < ob2)
```
## Output
<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/37ebd3ca-2557-4912-80c0-1f1003aa2c12" />

## Result
Thus To write a Python program that demonstrates operator overloading by overloading the less than (<) operator using a custom class has been executed sucessfully.

# 🐍 Python OOP: Polymorphism with Classes
## 🎯 AIM
To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism.

## 🧠 ALGORITHM
Create Class Beans:

Define type() method that prints "Vegetable". Define color() method that prints "Green". Create Class Mango:

Define type() method that prints "Fruit". Define color() method that prints "Yellow". Define Generic Function func(obj):

Call obj.type() and obj.color() — this works with both Beans and Mango objects, showcasing polymorphism. Create Objects:

Instantiate Beans and Mango. Pass them to func() and execute the program.

## 💻 Program
```
class Beans:
  def type(self):
      print("Vegetable")

  def color(self):
      print("Green")

class Mango:
  def type(self):
      print("Fruit")

  def color(self):
      print("Yellow")

def func(obj):
  obj.type()
  obj.color()

# Create objects
bean = Beans()
mango = Mango()

# Call func with both objects
func(bean)
func(mango)
```
## Output
<img width="1920" height="1080" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/f2cc05d4-6c63-454b-8e1f-6d853a869746" />

## Result
Thus To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism has been executed sucessfully
