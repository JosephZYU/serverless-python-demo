🧠 class (variables) -> instance.attriubtes:
1. **`Initializer Method`**
2. **`Instance Method (Regular Method)`**
3. **`Class Method`**
4. **`Static Method`**
5. **`Special Methods`**
___
- Classification of 5 common methods in Python Data Class:
   1. **`Initializer Method`**: Commonly known as a **`constructor`**, which initializes the state of new instances of a class.. It's a special method that initializes the state of new instances of a class.
        ```py
        def __init__(self, first, last, pay):
            self.first = first
            self.last = last
            self.email = first + '.' + last + '@email.com'
            self.pay = pay
        ```
   2. **`Instance Method (Regular Method)`**: Operates on an instance of a class and can modify object state and class state.
        ```py
        def fullname(self):
            return '{} {}'.format(self.first, self.last)

        def apply_raise(self):
            self.pay = int(self.pay * self.raise_amt)
        ```
   3. **`Class Method`**: Operates on the class itself and can modify class state that affects all instances.
    - A class method receives the class as an implicit first argument, usually named `cls`. It can modify class state that applies across all instances of the class.
        ```py
        @classmethod
        def set_raise_amt(cls, amount):
            cls.raise_amt = amount

        @classmethod
        def from_string(cls, emp_str):
            first, last, pay = emp_str.split('-')
            return cls(first, last, pay)
        ```
   4. **`Static Method`**: Similar to regular functions, they neither modify object state nor class state.
    - A static method does not receive an implicit first argument and behaves just like a plain function, but it belongs to the class's namespace.
        ```py
        @staticmethod
        def is_workday(day):
            if day.weekday() == 5 or day.weekday() == 6:
                return False
            return True
        ```
   5. **`Special Methods`**: Built-in methods for integrating with Python’s built-in functions or operator overloading. These methods allow customization of the behavior of Python's built-in or operator actions.
        ```py
        def __repr__(self):
            return "Employee('{}', '{}', {})".format(self.first, self.last, self.pay)

        def __str__(self):
            return '{} - {}'.format(self.fullname(), self.email)

        def __add__(self, other):
            return self.pay + other.pay

        def __len__(self):
            return len(self.fullname())
        ```
        - `__repr__`: The “official” string representation of an object. It is meant to be an unambiguous representation of the object and should be used for debugging.
        - `__str__`: The “informal” or nicely printable string representation of an object. It is meant to be readable and used for display purposes.
        - `__add__`: Method for the `+` operator. Defines behavior for when an instance of the class is used in an addition operation.
        - `__len__`: Method to return the length of the object, when passed to the `len()` built-in function.
        - `__init__`: Constructor for initializing new objects.
        - `__del__`: Destructor method for cleanup actions.
        - `__eq__`: Equality comparison (`==`).
        - `__ne__`: Inequality comparison (`!=`).
        - `__lt__`: Less than comparison (`<`).
        - `__gt__`: Greater than comparison (`>`).
        - `__le__`: Less than or equal to comparison (`<=`).
        - `__ge__`: Greater than or equal to comparison (`>=`).
        - `__getitem__`, `__setitem__`: Indexing and item assignment for collections.
        - `__iter__`, `__next__`: Making the object iterable.
        - `__call__`: Making the object callable like a function.
