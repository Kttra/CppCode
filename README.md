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

**Links to Other Helpful Projects**
------------
Here are some other projects that are similar to this one.

[Javascript Review](https://github.com/Kttra/JavascriptCode) - An overview of javascript

[C# Review](https://github.com/Kttra/CSharpCode) - An overview of C#

[Data Structures](https://github.com/Kttra/DataStructuresCSharp) - Repo where I cover some data structures.
