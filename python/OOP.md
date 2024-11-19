# **Object-Oriented Programming (OOP) in Python**

### **1. Classes**
- **Definition**: Blueprint for creating objects, bundling attributes (data) and methods (functions).
- **Syntax**:
  ```python
  class ClassName:
      def __init__(self, param):
          self.param = param

      def method_name(self):
          return f"{self.param} Method"
  ```
- **Example**:
  ```python
  class Car:
      def __init__(self, brand):
          self.brand = brand

      def display(self):
          return self.brand
  ```

---

### **2. Objects**
- **Definition**: Instances of a class.
- **Example**:
  ```python
  my_car = Car("Toyota")
  print(my_car.display())  # Toyota
  ```

---

### **3. Inheritance**
- **Single Inheritance**: One child inherits from one parent.
- **Syntax**:
  ```python
  class Parent:
      def greet(self):
          return "Hello"

  class Child(Parent):
      pass
  ```
- **Multiple Inheritance**: Child inherits from multiple parents.
  ```python
  class A: pass
  class B: pass
  class C(A, B): pass
  ```

---

### **4. Polymorphism**
- **Definition**: Same method name, different behavior in subclasses.
- **Example**:
  ```python
  class Animal:
      def sound(self): pass

  class Dog(Animal):
      def sound(self): return "Bark"

  class Cat(Animal):
      def sound(self): return "Meow"

  print(Dog().sound())  # Bark
  ```

---

### **5. Encapsulation**
- **Definition**: Restrict access to attributes and methods (use `_` or `__`).
- **Example**:
  ```python
  class Secure:
      def __init__(self):
          self.__secret = "Hidden"

      def reveal(self):
          return self.__secret
  obj = Secure()
  print(obj.reveal())  # Hidden
  ```

---

### **6. Abstraction**
- **Definition**: Hiding implementation details, focusing on functionality (via `abc` module).
- **Example**:
  ```python
  from abc import ABC, abstractmethod

  class Shape(ABC):
      @abstractmethod
      def area(self): pass
  ```

---

### **7. Method Overriding**
- **Definition**: Subclass redefines a method from the parent.
- **Example**:
  ```python
  class Base:
      def show(self): return "Base"
  class Sub(Base):
      def show(self): return "Sub"
  print(Sub().show())  # Sub
  ```

---

## **Resources**  

1. 🎥 **Playlist for OOP in Arabic**:  
   [OOP in Arabic on YouTube](https://youtube.com/playlist?list=PLUgz8T_NoattU54gGARPXPmmawQNl-1_T&si=iWtCSY7aD8pmublm)

2. 🎥 **Playlist for OOP in English**:  
   [OOP in English on YouTube](https://youtube.com/playlist?list=PL-osiE80TeTsqhIuOqKhwlXsIBIdSeYtc&si=Nri-oOE6MNmKxIdt) 

3. 🌐 **W3Schools Guide**:  
   [W3Schools - Python Classes](https://www.w3schools.com/python/python_classes.asp)  

4. 📖 **Official Documentation**:  
   [Python 3 Documentation](https://docs.python.org/3/)  
 
