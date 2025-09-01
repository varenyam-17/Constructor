# Constructors in C++

## 🎯 Aim
To understand the concept, types, and behavior of constructors in C++ and their role in object-oriented programming.

---

## 📚 Theory

A constructor is a special member function in C++ that is automatically invoked when an object of a class is created. Its primary purpose is to initialize objects and allocate resources if needed. Constructors are fundamental to object-oriented design, ensuring that objects begin their lifecycle in a valid and predictable state.

### 🔹 Key Characteristics

- **Same name as the class**: A constructor must have the exact name as its class.
- **No return type**: Constructors do not return values, not even `void`.
- **Automatic invocation**: Called implicitly when an object is instantiated.
- **Overloading supported**: Multiple constructors can exist with different parameter lists.

### 🔹 Types of Constructors

1. **Default Constructor**  
   - Takes no parameters.  
   - Automatically provided by the compiler if no other constructors are defined.  
   - Initializes members to default values (zero, empty string, etc.).

2. **Parameterized Constructor**  
   - Accepts arguments to initialize object members with specific values.  
   - Enables flexible object creation based on context or input.

3. **Copy Constructor**  
   - Takes a reference to another object of the same class.  
   - Used to create a new object as a copy of an existing one.  
   - Essential for managing deep copies when dealing with dynamic memory.

4. **Dynamic Constructor**  
   - Allocates memory during object creation using `new` or other dynamic techniques.  
   - Useful in classes that manage resources like arrays, files, or buffers.

5. **Constructor Overloading**  
   - Multiple constructors with different parameter types or counts.  
   - Allows objects to be initialized in various ways depending on the use case.

### 🔹 Constructor Behavior

- Constructors are invoked in the order of object creation.
- If a class has only parameterized constructors, the compiler does not provide a default constructor.
- Constructors can be declared `explicit` to prevent implicit conversions.
- Initialization lists (`: member(value)`) are preferred for initializing const or reference members.

### 🔹 Importance in OOP

- Promotes encapsulation by hiding initialization logic.
- Ensures consistency and safety in object creation.
- Supports polymorphism and inheritance through constructor chaining.
- Facilitates resource management and exception safety.

---

## ⚙️ Functions of Constructors

- Initialize object members with default or user-defined values.
- Allocate and manage resources during object creation.
- Enable object copying and cloning via copy constructors.
- Support multiple initialization paths through overloading.
- Provide a foundation for robust, maintainable class design.
## Algorithm:


### Copy Constructor:
1. Start  
2. Define a class  
   - Choose a class name  
   - Declare private data members  
3. Declare constructors  
   - Default constructor  
   - Parameterized constructor(s)  
   - Copy constructor (optional)  
4. Initialize members  
   - Use assignment or initialization lists  
5. Create objects  
   - Use different constructors:
     - `ClassName obj1;` → default  
     - `ClassName obj2(args);` → parameterized  
     - `ClassName obj3 = obj2;` → copy  
6. Verify initialization  
   - Use member functions to confirm values  
7. End
### Addition Using Constructor:
1. **Start**

2. **Define a class**  
   - Choose a class name (e.g., `Addition`)  
   - Declare private data members to store two numbers and their sum

3. **Create a parameterized constructor**  
   - Accept two arguments  
   - Initialize the data members with these values  
   - Perform addition inside the constructor and store the result

4. **Define a member function**  
   - Create a function to display the result of the addition

5. **In `main()` function**  
   - Create an object of the class using the parameterized constructor  
   - Call the display function to show the result

6. **End**
### Destructor:
1. **Start**

2. **Define a class**
   - Choose a class name (e.g., `Resource`, `FileHandler`)
   - Declare private data members (e.g., pointers, file handles, buffers)

3. **Create a constructor**
   - Initialize data members
   - Allocate resources if needed (e.g., dynamic memory, open files)

4. **Define a destructor**
   - Use `~ClassName()` syntax
   - Release or clean up resources:
     - Use `delete` or `delete[]` for dynamic memory
     - Close file handles or network connections
   - Optionally print a message to confirm destruction (for debugging)

5. **Create objects in `main()`**
   - Instantiate objects using constructor
   - Perform operations as needed

6. **Allow object to go out of scope**
   - Destructor is automatically invoked when object lifetime ends

7. **End**
   ### Parameterized Constructor Swap:
   1. **Start**

2. **Define a class**  
   - Name the class (e.g., `swap1`)  
   - Declare three private data members: `a`, `b`, and `temp`

3. **Create a parameterized constructor**  
   - Accept two integer arguments `x` and `y`  
   - Assign `x` to `a` and `y` to `b`  
   - Use `temp` to swap the values:
     - `temp = a`  
     - `a = b`  
     - `b = temp`

4. **Define a member function `disp()`**  
   - Display the values of `a` and `b` after swapping

5. **In `main()` function**  
   - Declare two integer variables `a` and `b`  
   - Prompt the user to input values for `a` and `b`  
   - Create an object of the class using the constructor with `a` and `b`  
   - Call the `disp()` function to show swapped values

6. **End**


## ✅ Conclusion


Constructors are a cornerstone of C++ class design. They automate and standardize object initialization, reduce errors, and enhance code clarity. Mastering constructors—including their types, behaviors, and best practices—is essential for writing efficient and reliable C++ programs.
