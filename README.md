# CppCode
C++ code reference. A quick review of C++. Some of the below concepts are covered in this doc file: [C++ Quick Review](https://github.com/Kttra/CppCode/blob/main/C%2B%2B%20Quick%20Review.docx).

**Using Namespace Std**
--------------
In this section, we will be using namespace std. When you use using namespace std, you are telling the compiler to look for identifiers in the std namespace if it can't find them in the global namespace. This means that you don't have to type std:: before every standard library function or object, which can save you time and make your code more readable.

Using namespace std in C++ has both benefits and disadvantages.

**Benefits:**

•  It saves time by not having to type std:: before every standard library function or object.

•  It makes the code more readable by reducing the amount of code that needs to be written.

**Disadvantages:**

•  It can cause naming conflicts if two libraries use the same name for a function or object.

•  It can make the code less readable if there are many functions and objects being used from the standard library.

It is generally considered bad practice to use using namespace std in header files because it can cause naming conflicts in other files that include the header file. It is better to use the std:: prefix in header files to avoid naming conflicts. In source files, it is generally acceptable to use "using namespace std" if it is used after all the header files have been included.

**Printing & Getting Userinput**
--------------
In C++, you can use the cout statement to print output to the console and the cin statement to get input from the user.

Here is an example of how to use cout to print output to the console:

```c++
#include <iostream>
using namespace std;

int main() {
  cout <<"Hello, World!";
  return 0;
}
```

This program will print "Hello, World!" to the console.

Here is an example of how to use cin to get input from the user:

```c++
#include <iostream>
using namespace std;

int main() {
  string name;
  cout <<"Enter your name: ";
  cin >>name;
  cout <<"Hello, " << name << "!";
  return 0;
}
```

This program will ask the user to enter their name, then print "Hello, " followed by their name.

**Datatypes**
--------------
In C++,there are three types of data types: primitive data types, abstract data types, and derived data types. Primitive data types are built-in or predefined data types and can be used directly by the user to declare variables. Some examples of primitive data types in C++ are integer, character, boolean, double floating-point, or void

Primitive data types available in C++ are:

•  int (integer)
```c++
int age = 50;
```
•  char (character)
```c++
char grade = 'A';
```
•  string (Instead of one character, it is a string of characters)
```c++
string phrase = "Hello World";
```
•  double (double floating-point)
```c++
double gpa = 2.3;
```
•  bool (boolean)
```c++
bool isMale = true;
```
•  void (valueless)

**Datatypes**
--------------
In C++, a string is a type of object representing a collection (or sequence) of different characters. Strings in C++ are a part of the standard string class (std::string).

```c++
string phrase = “hello world”;
phrase.length(); //11
phrase[0]; //h
phrase[0] = ‘a’; //aello world
phrase.find(“world”, 0); //look if hello exists starting at index 0, outputs 6
phrase.substr(6, 5); //parameters: starting index, length | returns "world" in this case
```

**Numbers \[#include \<cmath\>\]**
-----
The numerics library "cmath" contains mathematical operations.

```c++
10 % 3; \\ 10 mod 3, gives remainder 1
int wnum = 5;
double dnum = 5.5;
wnum++; \\6
wnum--; \\5
wnum += 20; \\25
pow(2,5); \\2^5 = 32
sqrt(36); \\6
round(4.1); \\4
round(4.6); \\5
ceil(4.1); \\5
floor(4.8); \\4
fmax(3,10); \\returns the maximum, 10 in this case
fmin(3,10) \\returns the minimum, 3 in this case
```
**User Input**
------------
In C++, you can use the cin object to read user input from the console. The cin object is an instance of the istream class and it is defined in the iostream header file.

```c++
cout << "Enter your age: ";
cin >> age;
cout << "You are " << age << " years old";
string name;
getline(cin, name); //Receives entire line as input
cin.ignore(); //used to ignore or clear one or more characters from the input buffer
```

**Arrays**
------------
In C++, an array is a collection of elements of the same data type, stored in contiguous memory locations. Arrays are used to store multiple values in a single variable, making it easier to organize data in the program.

```c++
int luckyNums[20] = {4, 8, 15, 16, 23, 42};
luckyNums[10] = 100;
luckyNums[2]; //15
```

**Functions**
------------
In C++, a function is a block of code that performs a specific task. Functions are used to break down large programs into smaller, more manageable pieces. There are different return types for a function. Below are a few examples.

•  void: This return type is used when the function does not return any value.

•  int: This return type is used when the function returns an integer value.

•  double: This return type is used when the function returns a floating-point value.

•  char: This return type is used when the function returns a single character.

•  bool: This return type is used when the function returns a boolean value.

```c++
void sum(int a, int b){
	return a + b;
}

```


**If Statements**
------------
An if statement is used to execute a block of code if a certain condition is true. The condition is a boolean expression that is evaluated to either true or false. If the condition is true, the code inside the if statement is executed. If the condition is false, the code inside the if statement is skipped.

```c++
if (condition) {
// code to execute if condition is true
}
```

An if statement can also be followed by an else statement, which is executed if the condition is false. The syntax for an if-else statement is as follows:

```c++
bool isMale = true;
if(isMale){
	cout << "You are male";
}
else{
	cout << "You are not male";
}
```

**Switch Statements**
----
A switch statement is used to execute a block of code based on the value of a variable.

```c++
switch (variable) {
case value1:
  //code to execute if variable equals value1
  break;
case value2:
  //code to execute if variable equals value2
  break;
  ...
default:
  //code to execute if variable does not equal any of the values
  break;
}
```

The break statement is used to exit the switch statement after a case is executed. If the break statement is not used, the code will continue to execute until a break statement is encountered or the end of the switch statement is reached.

**Loops**
----
For loops and while loops are used to execute a block of code repeatedly.

A for loop is used when the number of iterations is known in advance. The syntax for a for loop is as follows:

```c++
int num = 5;
for (int i = 0; i < num; i++) {
  //code to execute
}
```

The initialization is used to initialize the loop variable, the condition is used to test the loop variable, and the update is used to update the loop variable after each iteration. The code inside the for loop is executed as long as the condition is true.

A while loop is used when the number of iterations is not known in advance. The syntax for a while loop is as follows:

```c++
while (condition) {
  //code to execute
  //change condition to false eventually or break out of loop
}
```
The condition is a boolean expression that is evaluated to either true or false. The code inside the while loop is executed as long as the condition is true.

**2d Array & Nested Loops**
-----

In C++, a 2D array is an array of arrays. It is used to store a table of values, where each row and column has a unique index.

The syntax for a 2D array is as follows:
type arrayName[rowSize][colSize];

The rowSize and colSize are the number of rows and columns in the array, respectively. The type is the data type of the elements in the array.

Nested loops are used to iterate over a 2D array. The outer loop iterates over the rows, and the inner loop iterates over the columns. The syntax for a nested loop is as follows:

```c++
for (int i = 0; i < rowSize; i++) {
  for (int j = 0; j < colSize; j++) {
    //code to execute
  }
}

int numberGrid[3][2] = {{1, 2},
                        {3, 4}.
		        {5,6}};
for(int i=0;i<3;i++){
	for(int j = 0; j<2;j++){
		cout << numberGrid[i][j];
  }
}

```

**Progress**
------------
This is still a work in progress.

**Links to Other Helpful Projects**
------------
Here are some other projects that are similar to this one.

[Javascript Review](https://github.com/Kttra/JavascriptCode) - An overview of javascript

[C# Review](https://github.com/Kttra/CSharpCode) - An overview of C#

[Data Structures](https://github.com/Kttra/DataStructuresCSharp) - Repo where I cover some data structures.
