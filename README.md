## Ex1 : Python OOP: Abstract Class & Method Example

## AIM

To create an abstract class named Shape with an abstract method calculate_area, and implement this method in two subclasses: Rectangle and Circle.

## ALGORITHM

1. Import ABC module:
     Use from abc import ABC, abstractmethod to define abstract classes and methods.
2. Create Abstract Class Shape:
     Define an abstract method calculate_area() with @abstractmethod.
3. Create Subclass Rectangle:
     Set default values for length and breadth.
     Override calculate_area() to compute the rectangle area.
4. Create Subclass Circle:
     Set default value for radius.
     Override calculate_area() to compute the circle area.
5. Create Objects & Call Methods:
     Instantiate Rectangle and Circle.
     Call their calculate_area() methods.
   
## Program
```
from abc import ABC, abstractmethod
import math
class Shape(ABC):

    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def calculate_area(self):
        return self.width * self.height
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        return math.pi * (self.radius ** 2)
rect = Rectangle(5, 3)
print("Rectangle area:", rect.calculate_area())

circle = Circle(4)
print("Circle area:", circle.calculate_area())
```
## Output

<img width="391" height="60" alt="Screenshot 2026-03-29 191711" src="https://github.com/user-attachments/assets/ffce2e3e-d1d2-4e95-aee5-280515af0268" />

## Result

The program successfully calculates area of shapes using abstarct method and classes.


## Ex2 : Python OOP: Encapsulation with Private Members

## AIM

To implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth.

## ALGORITHM

1. Define the Class:
      Create a class Rectangle with two private attributes: __length and __breadth.
2. Initialize Variables:
      Use the __init__() constructor to set initial values for __length and __breadth.
3. Print Values:
      Display the private variables from within the class to demonstrate access.
4. Instantiate the Object:
      Create an object of the Rectangle class to trigger the constructor.
   
## Program
```
class Rectangle:
    def __init__(self, length, breadth):
        self.__length = length     
        self.__breadth = breadth   
    def display(self):
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)
rect = Rectangle(10, 5)
rect.display()
```
## Output

<img width="372" height="100" alt="Screenshot 2026-03-29 192238" src="https://github.com/user-attachments/assets/e17942e7-c2ad-4168-b2e6-cdb2071d16d4" />

## Result

The program successfully demonstrates Encapsulation in Python by defining a class with private data members (__length and __breadth). The private variables are accessed only through class methods, ensuring data protection and controlled access.


## Ex3 : Method Overriding-Fish and Shark Class Inheritance in Python

## AIM:

To write a Python program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method.

## ALGORITHM:

1. Define the Fish class with a method named type() that prints "fish".
2. Define the Shark class as a subclass of Fish, and override the type() method to print    "shark".
3. Create an instance of the Fish class named obj_goldfish.
4. Create an instance of the Shark class named obj_hammerhead.
5. Use a for loop to iterate over both objects.
6. Within the loop, call the type() method using the loop variable.
7. Output will demonstrate method overriding: printing "fish" and "shark" accordingly.
   
## PROGRAM:
```
class Fish:
    def type(self):
        return "I am a fish."
class Shark(Fish):
    def type(self):
        return "I am a shark, a type of fish."
fish = Fish()
print(fish.type()) 

shark = Shark()
print(shark.type())
```
## OUTPUT

<img width="374" height="70" alt="Screenshot 2026-03-29 192512" src="https://github.com/user-attachments/assets/da1864c3-bb7d-452c-9e05-43a2ddf0ed24" />

## RESULT

The program successfully creates class inheritance.


## Ex4 : Python OOP: Polymorphism with Classes

## AIM

To create two specific classes — Beans and Mango. Then, create a generic function that can accept any object and determine its type (Fruit or Vegetable) and color, using polymorphism.

## ALGORITHM

1. Create Class Beans:
      Define type() method that prints "Vegetable".
      Define color() method that prints "Green".
2. Create Class Mango:
      Define type() method that prints "Fruit".
      Define color() method that prints "Yellow".
3. Define Generic Function func(obj):
      Call obj.type() and obj.color() — this works with both Beans and Mango objects,          showcasing polymorphism.
4. Create Objects:
      Instantiate Beans and Mango.
      Pass them to func() and execute the program.

## Program
```
from abc import ABC, abstractmethod
class Food(ABC):
    @abstractmethod
    def get_type(self) -> str:
        pass

    @abstractmethod
    def get_color(self) -> str:
        pass
class Beans(Food):
    def get_type(self) -> str:
```
## Output

<img width="563" height="72" alt="Screenshot 2026-03-29 192817" src="https://github.com/user-attachments/assets/ad8f6941-c2d7-4a89-95da-067c79f05746" />

## Result

The program successfully creates class and returns type using polymorphism.
