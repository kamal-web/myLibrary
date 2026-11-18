History:
-------
We all know that digital computers  only know 1s and 0s, or binary. 
But interestingly, computers can represent  anything we want using only those two digits. 

any software program you write has to be  able to convert to and from binary data.

To illustrate this, let's get  a computer. But not everything, 
just the two most important components,  which are the CPU and the Memory or RAM.
And let's take a look at a  very simple Python program.

            print("Hello World");

Programs have two components; data and  some operations you apply on those data. 

Here we have one of each.
When we run the program, we  store these data in our memory. 
And then, we do the operations on the CPU.
In this case, it's a print operation  to print some output on the terminal.
So, we have the same problem again. 
How do we store "Hello World!" in our memory? Our Memory doesn't know anything about English characters to store them. It only knows binary.

The solution, as you might have  guessed, is called a Type System.

Every Programming Language should have Type System.

A type system of a programming  language has 2 responsibilities. 

1.First one as we discussed, is  conversion to and from binary data;  
also called serialization and deserialization.

To convert decimal numbers to binary,  
you can use base conversion as you  might remember from high school maths.

This is very easy.

But to convert any other data like strings,  you need some special conversion rules. 
There are universally standardized such rules, and the type system in your programming  language knows all of these rules.

In our example, to convert a string, type system  uses a character encoding rule called Unicode. 

With Unicode, each character in the  string is converted to a unique number,  
which can be converted to binary. 

So using this rule, you can convert the  "Hello World!" string to bunch of binary data.

Since there are different rules for different  types like  strings, decimal numbers, images, etc., your program also needs to keep track of the  type of this binary data chunk because later on, when you read this data, you need to know  which rule to apply for the conversion back. 

This information about the type  of the data is called a datatype.
So in our example, Python creates and saves "Hello World!" as a string-typed data  in binary format on the memory.
Ok, now we know how to store and read  different types of data from the memory. 
Next, without using the data as is,  you might also need to manipulate them. 
That is the second  responsibility of a type system. 

Defining rules for operations  on different data types.

Let's take an example of adding a  whole number to a decimal number.
        3.14+4 = 7.14 but not 3.18
It's a very simple thing to do  for you using basic mathematics. 

But for a software program,  it's a tiny bit complicated.
First of all, you should know  the types of these two data. 
That's easy enough. 
We discussed that the programming  language keeps track of the data type.
Next, it needs to know if the  addition operator is even possible, and then the rules behind adding a  whole number to a decimal number.

The rules are very simple, You just add the whole number part  of the decimal to the other whole number while keeping the fractional part intact. 
No matter how simple this is, type  system should know these rules.

So that's the second  responsibility of the type system. 

To know what operations are possible upon different data types, and the rules behind applying those operations.

With a type system that handles these two responsibilities, any programming language you use can read, store, and manipulate data quite seamlessly.

And that concludes what a Type System is.

-----------------------------------------------------------
The difference between a statically typed programming language  and dynamically typed programming language. Because there's this misconception that  dynamically typed programming languages like python and javascript doesn't have data types or a type system.
Python and JavaScript being  dynamically typed languages has nothing to do with having  a type system, actually. 
They also have a type system, and it has the  same responsibilities that we talked about similar to the type system in statically  typed languages like C++ or Java.
Do you remember I said that the programming  language keeps track of the type of the data?Well, how we keep track of this data type is what  differs from static typing to dynamic typing.
To know the difference between  static typing and dynamic typing, we first need to know what a variable is. Do you remember writing expressions  like these in middle school maths?
    x = 1
    y = 4
In this case, x and y are called variables.
Variables are a label you give  to a certain chunk of data. 
Once you have assigned a variable on some data, you can use the variable name to  access that data again from memory. Again, do you remember that we need to know  the data type when we read data from memory? 
How we keep track of this data type is different  
between statically typed languages  and dynamically typed languages.
In a statically typed language,  variables have a type, and it is decided when your program is created.
Most of the time, you, as a  programmer, has to define this type. 
When you try to access or modify the  data that the variable points to, we can use the type we defined  for the variable to do this.
In a dynamically typed language, variables  don't have a specific type defined to them. 
The type information is stored  alongside the data itself and your programming language has a way of  checking the data type first dynamically and then use that data type to read the data.
Now you might be thinking, why do we have  these two variants of programming languages?

First of all, Dynamically typed  languages are very easy to use in a way because you as a programmer,  doesn't have to think about data types.

I won't go into much details  about why static typing is useful, but statically typed languages can do a lot of checks on variables even  before the program is run.

So they can find if you made a mistake, like trying to do a sum up between an integer and  some image data even before you run the program. 
Dynamically typed languages can't do  that beforehand because they check the type dynamically when you run the program.

Anyway, getting back to the topic, now you see both Dynamically typed and  Statically typed languages, in fact, has types.
The type system is actually mandatory  for any programming language.
