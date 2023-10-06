### 1. What is the difference between a method defined with single underscore and a double underscore?

 - _get_list():

   - A method name starting with a single underscore _ is a convention in Python to indicate that the method is intended to be considered **private**. It's not a strict access control mechanism; it's more of a signal to other developers that the method is for internal use within the class or module and should not be accessed directly from outside the class or module.
   
   - It doesn't have any special name mangling or name alteration. It's just a regular method with its name starting with a single underscore.
   Developers can still access _get_list() from outside the class if they choose to, but it's considered good practice not to do so unless it's necessary.
   
 - __get_list():

   
   - A method name starting with a double underscore __ triggers **name mangling** in Python. *Name mangling is a mechanism that Python uses to make it harder to accidentally override methods and attributes in a subclass.* It changes the name of the method by adding **_ClassName** as a prefix to the method name.
  
   - For example, if you have a class named MyClass and you define a method __get_list(), Python will rename it to _MyClass__get_list() behind the scenes.
   The purpose of name mangling is to prevent accidental name conflicts when subclassing. It makes it more difficult for subclasses to accidentally override a method with the same name.
   
   ```python

   class MyClass:
      def _get_list(self):
         return "This is _get_list()"

      def __get_list(self):
         return "This is __get_list()"

   obj = MyClass()
   print(obj._get_list())   # Accessing _get_list() is allowed and common.
   # Output: This is _get_list()

   # Accessing __get_list() directly will raise an AttributeError.
   # print(obj.__get_list())  # Raises an AttributeError

   # Accessing the name-mangled version of __get_list() is possible.
    print(obj._MyClass__get_list())  # Output: This is __get_list()
   
   ```

### 2. OOPS Conecpts

 1. #### Why we use OOPS?
 
      - OOPs makes development and maintenance easier where as in Procedure-oriented programming language it is not easy to manage if code grows as project size grows.
      
      - OOPs provide data hiding whereas in Procedure-oriented programming language a global data can be accessed from anywhere.
      
      - OOPs provide ability to simulate real-world event much more effectively. We can provide the solution of real word problem if we are using the Object-Oriented Programming language.


 2. #### Building blocks of OOPS
   
      - Class
      - Object
      - Method
      - Inheritance
      - Polymorphism
      - Abstraction
      - Encapsulation
      - __init__ method or class Constructor
      - self variable
      - Instance variable
      - Class variable
      - Static method
      - Class method
      - Method Overriding
      - Method Overloading
      - super() method


### 3. What is Iterator and Generator?

### 4. What is the difference between range and xrange?

### 5. Why we use Generators? Have you implemented any custom made Generator?

### 6. What are the different data types in python? Are the tuple mutable? 
 - Mention the workaround if asked to make tuple mutable.

### 7. What are the packages and modules in python?

### 8. Explain how python works or explain the python internals?

### 9. Explain Function Overloading.

### 10. Explain Map, Reduce and Filter.

### 11. Explain Lambda function.

### 12. Explain Closures.

### 13. What is PIP and PEP8?   

### 14. What is the difference between the list and tuple?

### 15. What are forzensets?

### 16. What will happen if I create a dictory with duplicate keys?

### 17. How would you use a decorator in a method defined inside a class?

### 18. What is the zip() function in Python?

### 19. what is pass by value and pass by reference?

### 20. Explain the shallow copy and deep copy.

### 22. What are the namespaces in Python?

### 24. What is **nonlocal** keyword in Python?
 - In Python, the nonlocal keyword is used to declare a variable that is not local to the current scope, but instead comes from the nearest enclosing scope. This is useful for nested functions, as it allows the inner function to access variables that are defined in the outer function.

    ```python
    def outer():
    x = 10

    def inner():
        nonlocal x
        x += 1
        print(x)

    inner()

    outer()

    # Here the output will be 11``
    ```

### 24. What is the difference between the **is** and **==** operators in Python?

### 25. What is **Global** keyword in Python?


### 26. What is pass, continue and break in Python?

### 27. What is the difference between the **isinstance()** and **type()** functions?

### 28. What is the difference between the **deepcopy()** and **copy()** functions in Python?


## Rest will be added soon...............

