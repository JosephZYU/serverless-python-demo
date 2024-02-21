🧠 Instance vs. Variable vs. Attribute [Corey Schafer: Object-Oriented](https://github.com/CoreyMSchafer/code_snippets/tree/master/Object-Oriented)
   - **Instance**: The concrete realization of a class, where the class is a blueprint.
      - An individual object of a certain class. For example, `emp1` and `emp2` can be instances of the `Employee` class.
   - **Variable**: A named storage that holds a value and is associated with an object or class.
      - A storage location paired with an associated symbolic name, which contains some known or unknown quantity of information referred to as a value. For example, `raise_amt` in the `Employee` class is a variable.
   - **Attribute**: Typically refers to the properties associated with a specific instance (often accessed with `self.attribute_name` in instance methods).
      - A value associated with an object which is referenced by name using dotted expressions. For example, `self.first` in the `Employee` class is an attribute.
      - When you see `self`, it refers to the instance on which the method is called. It is used to access attributes and methods of the object. For instance, `self.first` accesses the `first` attribute of the specific instance of `Employee`.
