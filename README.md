# C# Tafe Course
Written by Brook Jeynes and {put tafe teachers name}
<br>
# Getting Started
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

# Running your first project
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
<h1>Creating your first C# application</h1>
Start off by creating a file called main.cs and then add the code below into it, save, and run
<br>

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
<h1>Variables</h1>
Variables store data which can then be referenced later by using that variable name. Variables can hold many types of data and must be declared when creating that variable.

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

