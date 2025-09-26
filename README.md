
---

📘 Constructors & Destructors in C++


---

🎯 Aim

To understand, use, and implement C++ Constructors and Destructors, exploring their role in object initialization, cleanup, and lifecycle management.


---

📚 Theory

In C++, constructors and destructors are special member functions that manage the lifecycle of an object — from creation to destruction.


---

🏗️ Constructor

A constructor is a special member function that is automatically invoked when an object of a class is created.
Its purpose is to initialize data members so the object starts in a valid state.

Key Characteristics:

Same name as class.

No return type.

Invoked automatically.

Can be overloaded.


Types of Constructors:

1. Default Constructor


2. Parameterized Constructor


3. Copy Constructor


4. Delegating Constructor (C++11+)


5. Explicit Constructor




---

🗑️ Destructor

A destructor is a special member function that is automatically invoked when an object’s lifetime ends.
Its purpose is to release resources like memory, files, or connections.

Key Characteristics:

Same name as class but prefixed with ~.

No return type, no parameters.

Cannot be overloaded.

Only one destructor per class.


Order of Destruction:

Local objects: destroyed at scope end (reverse order of creation).

Global/static: destroyed at program termination.

In inheritance: derived destructor runs first, then base.



---

🔄 Constructor–Destructor Lifecycle

1. Memory allocation


2. Constructor call (initialization)


3. Object use (program logic)


4. Destructor call (cleanup)


5. Memory deallocation



This implements RAII (Resource Acquisition Is Initialization).


---

📋 Algorithms


---

🧾 Destructor with Global Counter

Steps:

1. Start


2. Define a global counter count = 0.


3. Class Student:

Constructor → increment & print number of objects created.

Destructor → decrement & print number of objects destroyed.



4. In main():

Create multiple objects.

Use a nested scope to show scope-based destruction.

End of main() destroys remaining objects.



5. End




---

📋 Copy Constructor

Steps:

1. Start


2. Class Student with members name, age, roll_no.


3. Parameterized constructor → initializes members.


4. Copy constructor → duplicates another object + prints a message.


5. display() → prints details.


6. In main():

Create s1 with parameterized constructor.

Copy s1 into s2 (copy constructor).

Display both.



7. End




---

📅 Parameterized Constructor

Steps:

1. Start


2. Class Date with members d, m, y.


3. Parameterized constructor → assigns day, month, year.


4. display() → prints d/m/y.


5. In main():

Take input for date.

Create object d1 using constructor.

Display.



6. End




---

🧑‍🎓 Default Constructor

Steps:

1. Start


2. Class Student with members name, fee.


3. Define a default constructor:

Assign default values like "Unknown" and 0.

Or take input from user.



4. display() → prints student details.


5. In main():

Create object s1 (calls default constructor automatically).

Display.



6. End




---
