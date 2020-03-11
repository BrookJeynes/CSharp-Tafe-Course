# C# Tafe Course
Written by Brook Jeynes and Robert MacKenzie
<br>
<h1>Getting Started</h1>
<h2>The IDE</h2>
We'll start off by installing <a href="https://visualstudio.microsoft.com/vs/community/">Visual Studio</a> however, feel free to use any IDE you feel comfortable with. It's important to know your way around the IDE of use so make sure to read documentation and at least know the basics of it.
<br>
<h2>Resources</h2>
This tutorial follows on from these online recources and gives some practice examples to complete to test your progress, it's not required but recommended you at least check out these resources for a better understand of basics: <h6 style="font-size:11px;"><i>*note: Many examples found in this document are taken and modified from various sites</i></h6>
<ul>
  <li><a href="https://channel9.msdn.com/Series/CSharp-Fundamentals-for-Absolute-Beginners?l=Lvld4EQIC_2706218949">C# Fundamentals for Absolute Beginners - <i>Channel 9</i></a></li>
  <li><a href="https://www.csharp-examples.net/">C# Code Examples</a></li>
  <li><a href="https://www.codeproject.com/KB/cs/">C# Project Examples</a></li>
</ul>
<hr>
<br>

<h1>Running your first project</h1>
In this section you will learn to
<ul>
  <li>Run a basic program</li>
  <li>Debug your program</li>
  <li>Understand coding terms and code pieces</li>
    <ul>
      <li>Using</li>
      <li>Namespaces</li>
      <li>Classes</li>
      <li>Content</li>
    </ul>
</ul>
<br>
<h2>Creating your first C# application</h2>
Start off by creating a file called main.cs and then add the code below into it, save, and run
<br><br>

```csharp
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World!");    
    }
  }
}
```

<h6 style="font-size:11px;"><i>*note: 
  <ul>
    <li>// will comment out a line</li> 
    <li>/* will comment out a section */</li>
  </ul></i>
</h6>

<br>

So what does this program actually do? This application will output the phrase "Hello World!" into the commandline. This project is the starting point of every programmers langauge learning journey. Lets now delve into what each line in this program does for a better understanding of C#.
<br><br>

```csharp
using System;
```

This first line of code is called a `Namespace`. A Namespace is an element in C# code used to organise your programs and, once created, allow you to reference parts of code from that namespace for later functions in the code. 

So what is the `System` namespace and what does it include?
> "The System namespace contains fundamental classes and base classes that define commonly-used value and reference data types, events and event handlers, interfaces, attributes, and processing exceptions." - <a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a>
<br><br>

```
namespace HelloWorld {
...
}
```

This line of code should be easy to interpret considering the previous analysis of the `System` namespace. In this line of code we create our own namespace labeled `HelloWorld`.
<br><br>

```
class Program {
...
}
```



<h6 style="font-size:11px;"><i>*note: for more information on namespaces and System check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/namespaces">What is a  Namespace?</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a></li> 
    <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system?view=netframework-4.8">What the System Namespace does</a></li>
  </ul></i>
</h6>

<br>
<h2>Variables</h2>
Variables store data which can then be referenced later by using that variable name. Variables can hold many types of data and must be declared when creating that variable.
<br><br>

```csharp
int bobAge = 100;
string bobAddress = "200 Old Man Street"
```
<br>
Here is a short list of the most common variable types
<ul>
  <li>Int: Stores integers (whole numbers), without decimals, such as 123 or -123</li>
  <li>Double: Stores floating point numbers, with decimals, such as 19.99 or -19.99</li>
  <li>Char: Stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes</li>
  <li>String: Stores text, such as "Hello World". String values are surrounded by double quotes</li>
  <li>Bool: Stores values with two states: true or false</li>
</ul>
<hr>
<br>

<h1>Data Types and Type Casting</h1>
<h2>User Input</h2>
Here is an example of a program that will check whether an entered number is odd or even. Write out the program in a new .cs file and try analyse the project and think about what it does before running it. After this we will breakdown what the project does, how and why it does what it does
<br><br>

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
 
namespace check1
{
    class Program
    {
        static void Main(string[] args)
        {
            int i;
            Console.Write("Enter a Number : ");
            i = int.Parse(Console.ReadLine());
            if (i % 2 == 0)
            {
                Console.Write("Entered Number is an Even Number");
                Console.Read();
            }
            else
            {
                Console.Write("Entered Number is an Odd Number");
                Console.Read();
            }
        }
    }
}
```
