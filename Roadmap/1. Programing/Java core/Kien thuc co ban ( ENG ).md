1. What is Java
**Java** is a programming language that is modern, easy to use, and secure. It is also a platform because it has a special environment (JVM) where Java code can run on any device.

2. JDK, JRE, JVM
**JDK (Java Development Kit)** is a toolkit that includes everything needed to create and run Java programs. It has two main parts:

- Development tools (for writing and building Java programs)
- JRE (for running Java programs)

**JRE (Java Runtime Environment)** is a package that provides an environment to run Java programs, but it does not have tools for creating Java programs. It’s used by end-users who just need to run Java applications, not develop them.

**JVM (Java Virtual Machine)** is the key part of both JDK and JRE. It runs Java programs line by line, so it’s often called an interpreter. Every Java program goes through the JVM, which makes the program run on any device with JVM installed.

3. Heap vs Stack 
**Heap** is memory used at runtime to store objects. Whenever you create an object using `new`, it is stored in the heap. Heap memory is generally larger than stack memory and is used for long-term storage of data while the program runs.

**Stack** is memory for storing local variables inside methods, including primitive types (like `int`, `char`) and references to objects in the heap. Stack variables usually have a short lifespan, as they are created when a method is called and cleared when the method ends.

4. What happens if you declare `static public void` instead of `public static void`?
The program will compile and run correctly.

5. What is the default value of local variables?
**Answer:** Local variables do not have a default value.

6. Explain the `final` keyword in Java.
**Answer:** The `final` keyword in Java is used to declare variables, methods, and classes that cannot be changed.
- **Variable**: The value cannot be changed once assigned. If it is not initialized, it can be assigned in the constructor.
- **Method**: The method cannot be overridden in subclasses.
- **Class**: The class cannot be extended (inherited).

7. What is `static` in Java?

**Answer:** In Java, `static` means that a method or variable belongs to the class, not to any specific object. All objects of the class share the same static variable or method.
- A **static variable** is shared by all instances of the class.
- A **static method** can only access other static variables or methods. It can be called without creating an object of the class.

8. Question: What is the difference between equals() and == in Java?

Answer:
- == compares the memory addresses of two objects, meaning it checks if they are the exact same object.
- equals() compares the values of two objects, meaning it checks if their contents are the same.
Example:
String str1 = new String("Hello");
String str2 = new String("Hello");
boolean referenceComparison = (str1 == str2); // false (different objects)
boolean contentComparison = str1.equals(str2); // true (same content)


9. **Question:** What is the difference between `String`, `StringBuffer`, and `StringBuilder` in Java?

**Answer:**
- **String** is **immutable**, meaning once a String object is created, it cannot be changed. Every time you modify a String, a new instance is created, which can be slow and memory-intensive.
    
- **StringBuffer** is **mutable**, meaning it can be modified. It is **synchronized**, making it thread-safe, so it is safe for use in multi-threaded environments, but it may be slower compared to `StringBuilder`.
    
- **StringBuilder** is **mutable** like `StringBuffer`, but it is **non-synchronized**, meaning it is not thread-safe. This makes it faster than `StringBuffer` when thread safety is not required.

10.What is `instanceof` in Java?

**Answer:** The `instanceof` operator is used to check if an object is an instance of a specific class or its subclass

11. What primitive types do you know?
8 primitive data types: byte, short, int, long, float, double, boolean, char.

12. What is the String Pool in Java?

**Answer:** The String Pool is part of the heap memory in Java, where String objects are stored. When you create a string, the JVM checks if the string already exists in the pool:

- If it exists, it returns a reference to that string.
- If not, it creates a new String object and stores it in the pool.


13. What is the Java Collections Framework?

**Answer:** The Java Collections Framework is a set of classes and interfaces in Java that provides data structures and algorithms to store, manage, and manipulate data.

14. What is the difference between Array and ArrayList in Java?

**Answer:**
- **Array** has a fixed size, while **ArrayList** starts with a size of 10 and can grow automatically.
- **Array** can store both primitive types (e.g., `int`) and objects, while **ArrayList** can only store objects. If you add a primitive type like `int`, it will be automatically converted using auto-boxing.
- **Array** is faster for storing data.
- **Array** has only one property (length).


15. What are the main interfaces of the Java Collections Framework?

**Answer:**
- **Collection**: The root interface for all collections, representing a group of objects.
- **List**: Inherits from Collection, allows ordered elements and duplicates. Examples: ArrayList, LinkedList.
- **Set**: Also inherits from Collection, does not allow duplicates and has no order. Examples: HashSet, TreeSet.
- **Queue**: Inherits from Collection, stores elements in the order they were added, often used for queue tasks. Examples: LinkedList, PriorityQueue.
- **Map**: Does not inherit from Collection, stores key-value pairs. Examples: HashMap, TreeMap.
- **SortedSet**: Inherits from Set, stores elements in natural order or by a Comparator.
- **SortedMap**: Inherits from Map, stores key-value pairs in the natural order of keys or by a Comparator.


16. **Question:** What is the difference between List and Set?

**Answer:**
- **Order**:
    - **List**: Stores elements in order and allows access by index.
    - **Set**: No specific order, does not guarantee the order of elements.
- **Duplicates**:
    - **List**: Allows duplicate elements.
    - **Set**: Does not allow duplicate elements; each element must be unique.
- **Implementing classes**:
    - **List**: Common classes include ArrayList, LinkedList.
    - **Set**: Common classes include HashSet, TreeSet.
- **Performance**:
    - **List**: Performance for operations like adding, removing, and accessing elements can vary depending on the List type.
    - **Set**: Adding and removing operations can be faster with HashSet due to the use of hashing.

17. Can you explain the difference between ArrayList and LinkedList?

**Answer:**

|**ArrayList**|**LinkedList**|
|---|---|
|Uses less memory.|Uses more memory (because it stores references to previous and next nodes).|
|Operations like adding and removing are slower.|Operations like adding and removing are faster.|
|Efficient access to data due to using an index.|Slower access to data, as it requires traversing nodes.|
|Works only as a list.|Can function as a list, stack, or queue.|
|Best for storing similar types of data.|Can store any type of data.|
|Uses a dynamic array to store elements.|Uses a doubly linked list to store elements.|

**When to use:**

- **ArrayList**: Best when you need fast access to elements and don't change the size often.
- **LinkedList**: Best when you frequently add or remove elements, especially at the beginning or end of the list.


18. What is a HashSet and how does it work?

**Answer:** A `HashSet` uses an internal `HashMap` to store elements. When an element is added, it is used as the key, and a dummy object is used as the value. This way, `HashSet` ensures each element is unique.

19. What are generics and how do they relate to collections?

**Answer:** Generics let you create data structures that work with different data types without needing to cast types when using them.

For example, you can define a class `Box<T>`, which can hold any data type (like `Integer`, `String`, etc.) by using the type parameter `T`.

19. What is the difference between HashSet and HashMap?

**Answer:**

- **HashSet**: Stores only unique elements with no specific order. It does not allow duplicate elements and has no index-based access.
    
- **HashMap**: Stores key-value pairs with unique keys (values can be duplicated). If you add a duplicate key, the new value will replace the old one.

20. What is OOP?

**Answer:** OOP (Object-Oriented Programming) is a model in software design that helps improve productivity, simplify maintenance, and make systems easy to expand. It introduces concepts like:

- **Object**
- **Class**
- **Inheritance**
- **Polymorphism**
- **Abstraction**
- **Encapsulation**

21. What are the main principles of Object-Oriented Programming (OOP)?

**Answer:** There are 4 main principles:

- **Inheritance**: Allows a class (child class) to inherit properties and methods from another class (parent class), which helps in code reuse.
    
- **Encapsulation**: Hides the data of an object from other objects, allowing access only through public methods.
    
- **Abstraction**: Hides internal details and shows only essential features. It allows you to define a class or method without specifying the full details.
    
- **Polymorphism**: Allows a method to have different implementations. This can be achieved through method overriding or method overloading.

22. What are Access Modifiers in Java?

**Answer:**

- **Public**: Accessible from everywhere.
- **Protected**: Accessible outside the package but only by subclasses.
- **Default** (no modifier): Accessible within the same package.
- **Private**: Accessible only within the same class.

23. What is `super` in Java?

**Answer:** `super` is a reference to the closest parent class. It is used in three main ways:

1. To access instance variables from the parent class.
2. To call the parent class’s constructor using `super()`.
3. To call methods from the parent class.


24. What is the difference between Abstract Class and Interface in Java?

**Answer:**

| **Abstract Class**                                                                | **Interface**                                                                               |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| 1) Can have both **abstract** (no body) and **non-abstract** (with body) methods. | Has only **abstract** methods. From Java 8, it can have **default and static** methods too. |
| 2) **Does not support multiple inheritance**.                                     | **Supports multiple inheritance**.                                                          |
| 3) Can have **final, non-final, static, and non-static** variables.               | Has only **static and final** variables.                                                    |
| 4) Can provide **implementation for interface methods**.                          | Cannot provide **implementation for abstract class methods**.                               |
| 5) Declared with the **abstract** keyword.                                        | Declared with the **interface** keyword.                                                    |
25. What are the `equals()` and `hashCode()` methods in Java?

**Answer:**

- **`equals()`**: Used to check if two objects are "equal" in terms of content. By default, `equals()` in the `Object` class checks memory addresses, but it can be overridden to compare actual data inside objects.
    
- **`hashCode()`**: Returns an integer value (hash code) for an object. It is used in hashing data structures like `HashMap` and `HashSet` to quickly locate objects. If two objects are equal according to `equals()`, they should have the same `hashCode()`.

26. What is the difference between Checked and Unchecked Exceptions in Java?

**Answer:**
- **Checked Exceptions**: These exceptions are checked at compile-time. The code must either handle these exceptions using a `try-catch` block or declare them with the `throws` keyword. Examples: `IOException`, `SQLException`.
- **Unchecked Exceptions**: These exceptions are not checked at compile-time. They are usually caused by programming bugs, like logic errors or invalid input. These exceptions are subclasses of `RuntimeException`. Examples: `NullPointerException`, `ArrayIndexOutOfBoundsException`.

