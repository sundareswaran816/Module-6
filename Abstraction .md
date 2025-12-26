# Python OOP: Abstract Class & Method Example

## AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## Program
```
from abc import ABC, abstractmethod
class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass
class Rectangle(Shape):
    def __init__(self):
        self.length = 10
        self.breadth = 5
    def calculate_area(self):
        return self.length * self.breadth
class Circle(Shape):
    def __init__(self):
        self.radius = 7
    def calculate_area(self):
        return 3.14 * self.radius * self.radius
rect = Rectangle()
cir = Circle()
print("Area of Rectangle:", rect.calculate_area())
print("Area of Circle:", cir.calculate_area())
```
## Output
![alt text](1.png)

## Result
Thus, the Python program successfully demonstrates the use of an abstract class and abstract method, with proper implementation in the Rectangle and Circle subclasses.