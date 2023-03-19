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

**Links to Other Helpful Projects**
------------
Here are some other projects that are similar to this one.

[Javascript Review](https://github.com/Kttra/JavascriptCode) - An overview of javascript

[C# Review](https://github.com/Kttra/CSharpCode) - An overview of C#

[Data Structures](https://github.com/Kttra/DataStructuresCSharp) - Repo where I cover some data structures.
