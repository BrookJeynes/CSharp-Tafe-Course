# C# Tafe Course
Written by Brook Jeynes and Robert MacKenzie
<br>

<h1>Table of Contents</h1>
<ul>
  <li><a href="#first-project">First Project</a></li>
  <ul>
    <li><a href="#creating-first-project">Creating your first project</a></li>
    <li><a href="#namespaces">Namespaces</a></li>
    <li><a href="#classes">Classes</a></li>
    <li><a href="#methods">Methods</a></li>
    <li><a href="#printing">Printing to the command line</a></li>
    <li><a href="#prject1">Project 1</a></li>
  </ul>
  <li><a href="#second-project">Math and C#</a></li>
  <li><a href="#resources-content">Resources</a></li>
</ul>

<hr> <br>

<h1>Getting Started</h1>
<h2>The IDE</h2>
We'll start off by installing <a href="https://visualstudio.microsoft.com/vs/community/">Visual Studio</a> however, feel free to use any IDE you feel comfortable with. It's important to know your way around the IDE of use so make sure to read documentation and at least know the basics of it.
<br>
<h2>Resources</h2>
This tutorial follows on from these online recources and gives some practice examples to complete to test your progress, it's not required but recommended you at least check out these <a href="#resources-content">resources</a> for a better understand of basics

<h6 style="font-size:11px;"><i>*note: Many examples found in this document are taken and modified from various sites. A complete resource list can be found <a href="#resources-content">here</a></i></h6>

<hr> <br>

<h1 id="first-project">Running your first project</h1>
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
<h2 id="creating-first-project">Creating your first C# application</h2>
It is advised that you create a new folder with each project and lesson as to make sure everything is easy to find and organised. <br>

```cmd
~$ mkdir "csharp tafe course"
~$ cd "csharp tafe course"
```

```cmd
~$ mkdir "examples"
~$ mkdir "projects"
~$ cd "examples"
```

<br>

For this example project we will create a new folder with the name "Hello World Example". <br>

```cmd
~$ mkdir "1 hello world"
~$ cd "1 hello world"
```

<br>

Once your folders are created it's time to create the .cs file. <br>

<i>Windows:</i>

```cmd
~$ echo $null >> main.cs
```

<i>Linux/Mac:</i>

```bash
~$ touch main.cs
```

<br>

Once you have created the `main.cs` file open it up in visual studio, or your IDE of choice, and make sure that you can connect to that project through the IDE editor. Now you have set everything up, write out the example code below. Try think about what it does before running it. <br><br>

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
It's important to note that the topics discussed below will be later discussed in more detail, this is just a simple overview as so you get a basic idea of C# and to not overload your brain with information.

<br>

<h3 id="namespaces">Namespaces</h3>

```csharp
using System;
```

<br>

This first line of code is called a `Namespace`. A Namespace is an element in C# code used to organise your programs and, once created, allow you to reference parts of code from that namespace for later functions in the code. 

So what is the `System` namespace and what does it include? <br>

> "The System namespace contains fundamental classes and base classes that define commonly-used value and reference data types, events and event handlers, interfaces, attributes, and processing exceptions." - <a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a>

<br>

The `using` keyword is equivalent to the `import` keyword. It allows you to import, or "use", that particular namespace (i.e. function)
<br><br>

```csharp
namespace HelloWorld {
...
}
```

<br>

This line of code should be easy to interpret considering the previous analysis of the `System` namespace. In this line of code we create our own namespace labeled `HelloWorld`.

<h6 style="font-size:11px;"><i>*note: for more information on namespaces and System check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/namespaces">What is a  Namespace?</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a></li> 
    <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system?view=netframework-4.8">What the System Namespace does</a></li>
  </ul></i>
</h6>

<br>

<h3 id="classes">Classes</h3>

```csharp
class Program {
...
}
```

<br>

Here we create a `class` and label it `Program`. A class is a <br>

> "...basic concept of Object-Oriented Programming which revolve around... real-life entities" - <a href="https://www.geeksforgeeks.org/c-sharp-class-and-object/">Geeks for Geeks - Class and Object</a>

<br>

It's essentially a user-defined blueprint which the interpretor uses to create an `Object`. 
In that quote you saw the phrase `Object-Oriented Programming` and `Object`, don't worry about these terms just yet because they will be discussed later. {add link to where they are discussed}

<h6 style="font-size:11px;"><i>*note: for more information on OOP, Objects and Classes check out these resources
  <ul>
    <li><a href="https://www.geeksforgeeks.org/c-sharp-class-and-object/">Classes and Objects</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes">A Guide to Classes</a></li> 
    <li><a href="https://en.wikipedia.org/wiki/Object-oriented_programming">What Object-Oriented Programming (OOP)</a></li>
  </ul></i>
</h6>

<br>

<h3 id="methods">Methods</h3>

```csharp
static void Main(string[] args) {
...
}
```

<br>

This is what we call a `Method`. A method is similar to a `Function` in other programming languages. The `Main` method is called in the above code. The main method is the first method (function) to be called when initially running the program. This means that nearly all the code you write will be inside the `Main()` method. 

For now we won't talk about what `static void` and `(string[] args)` means just yet, they will be discussed later however, if you want to read about them now some links to more information will be located just below.

<h6 style="font-size:11px;"><i>*note: It is important to note that throughout this document `method` and `function` are interchangeably used, they both mean the same thing. a method is a function and a function is a method</i></h6>

<h6 style="font-size:11px;"><i>*note: for more information on Methods check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/main-and-command-args/">Main Method</a></li>
    <li><a href="https://www.quora.com/Why-do-we-use-static-void-main-string-args-in-C">breakdown of a method</a></li> 
  </ul></i>
</h6>

<br>

<h3 id="printing">Printing to the console</h3>

```csharp
Console.WriteLine("Hello World!");
```

<br>

Finally onto the last line of this small program, if any of these concepts haven't made much sense don't worry too much as they will be covered later in the document. This was just a small rundown on basic concepts from a beginner application for people who don't have very much knowledge on C#. It is recommended however that further research into misunderstood topics to be done as all the example applications will build upon these basic concepts with the addition of more concepts.

In this line we have a couple things to talk about and we'll start with `Console.`. What is this? This is actually a `namespace`, remember from above how we used a namespace by importing it? (`using System;`). Here we use the namespace `Console` but you may be thinking, why didn't we import it? dont we have to import it to use it? Well, kind of. 

If we imported it the application would look like this instead: <br><br>

```csharp
using System;
using Console;

...{
  ...{
    ...{
      WriteLine("Hello World!");
    }
  }
}
```

<br>

If we import `Console` we can use any function inside of the namespace without needing to declare it. `WriteLine` is a function inside the `Console` namespace however, because we didn't reference (import) it at the start of the application we declared it as we used the functuion. Thats why in the line `Console.WriteLine(...);` we declare it.

So we've now declared the `Console.` namespace, what does the `WriteLine();` function do? It does exactly what it looks like it does, it prints out to the command line whatever is inside the function (inside the () brackets). 

We will talk about data types in the next section of this document but as of currently just remember:
<ul>
  <li>  
    A `String` is a series of characters and are declared by surrounding them in quotation marks (single '' or double "" work the same way). Example: "This is a string", "A string can include numbers aswell, 1 or 4 or maybe even 7"
  </li>
  <li>   
    An int (short for integer) is a series of numbers and are <b>not</b> contained in quotation marks, these are numbers that don't include decimal points
  </li>
</ul>

<h6 style="font-size:11px;"><i>*note: for more information on Methods check out these resources
  <ul>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system.console.writeline?view=netframework-4.8">WriteLine() method</a></li>
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/strings/">What are Strings</a></li> 
    <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types">What are Integers</a></li> 
  </ul></i>
</h6>

<br>

<h1 id="project1">main.cs: A Project About Structuring Your Programs</h1>
Now that you've learnt the structure of a C# program it's your time to have a go at creating one. Throughout this document there will be examples and mini projects for you to test your knowledge and to allow a hands on learning experience. <br>

The goal of this project is to, using the .cs file we just created, code a program which outputs the text `"C# is fun"` to the command line. Goodluck.

<h6 style="font-size:11px;"><i>*note: Underneath is an answer to this project, it is highly advised you take an attempt at the project before viewing the answer. Also note that there is never 1 single way to create a projects answer, everyone codes different and therefore there are many solutions to a single question. For this reason it is important to realise your answer may not match the one provided below, it is just a basic guide of our interpretation of the answer as long as your program does what the question asks, you have succeeded.</h6>

<br>
<h3>Project 1 Answer</h3> <br>

```csharp
using System;

namespace Project1
{
    class Program
    {
        static void Main(string[] args) 
        {
            Console.WriteLine("C# is fun")
        }
    }
}
```

<br>

Once you have finished the above program you are ready to move onto the next section

<hr> <br>

<h1 id="second-project">Variables, Data Types and Math</h1>
In this section you will learn to
<ul>
  <li>Create Variables</li>
  <li>Take User Input</li>
  <li>Do Math in C#</li>
  <li>Data Type Casting</li>
</ul>
<br>
<h2>Variables</h2>
Variables store data which can then be referenced later by using that variable name. Variables can hold many types of data but that data type should always be declared when creating it.
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

<h1 id="resources-content">Complete Resource List</h1>

<h2>C# Code/Project Examples</h2>
<ul>
  <li><a href="https://channel9.msdn.com/Series/CSharp-Fundamentals-for-Absolute-Beginners?l=Lvld4EQIC_2706218949">C# Fundamentals for Absolute Beginners</a></li>
  <li><a href="https://www.csharp-examples.net/">C# Code Examples</a></li>
  <li><a href="https://www.codeproject.com/KB/cs/">C# Project Examples</a></li>
</ul>

<h2>Namespaces</h2>
<ul>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/language-specification/namespaces">What is a  Namespace?</a></li>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/namespaces/">A Guide to Namespaces</a></li> 
  <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system?view=netframework-4.8">What the System Namespace does</a></li>
</ul>

<h2>Classes, Objects and Object-Oriented Programming</h2>
<ul>
  <li><a href="https://www.geeksforgeeks.org/c-sharp-class-and-object/">Classes and Objects</a></li>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes">A Guide to Classes</a></li> 
  <li><a href="https://en.wikipedia.org/wiki/Object-oriented_programming">What Object-Oriented Programming (OOP)</a></li>
</ul></i>

<h2>Methods</h2>
<ul>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/main-and-command-args/">Main Method</a></li>
  <li><a href="https://www.quora.com/Why-do-we-use-static-void-main-string-args-in-C">breakdown of a method</a></li> 
</ul></i>

<h2>WriteLine Methods and Strings/Integers</h2>
<ul>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/api/system.console.writeline?view=netframework-4.8">WriteLine() method</a></li>
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/strings/">What are Strings</a></li> 
  <li><a href="https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/integral-numeric-types">What are Integers</a></li> 
</ul></i>

