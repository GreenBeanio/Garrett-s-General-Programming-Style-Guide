# Garrett's General Programming Style Guide

## Version: 1.0

# Table of Contents

- [Readability](#Readability)
- [Headers](#Headers)
- [Footers](#Footers)
- [Comments](#Comments)
- [Documentation](#Documentation)
- [Naming Conventions](#Naming_Conventions)
- [Naming Rules](#Naming_Rules)
- [Exception Handling](#Exception_Handling)
- [Maximum Line Length](#Max_Line_Length)
- [Blank Lines](#Blank_Lines)
- [Indentation](#Indentation)
- [Curly Brackets](#Curly_Bracket)
- [Parentheses](#Parentheses)
- [Semicolon](#Semicolon)
- [Quotes](#Quotes)
- [Max Nesting Levels](#Max_Nesting_Levels)
- [Optimization](#Optimization)
- [Principle of Least Privilege](#PLP)
- [General Programming Language Information](#PLA)

---

# Preamble

This document serves as a general style guide to be used across various programming languages. This is a style guide that I am creating for myself. The most important part of this style guide will be the naming conventions, as these will stay consistent across most languages. Other aspects regarding syntax and such can change depending on the language. If you decide to use this style guide, feel free to modify it in any way that makes your code more consistent. Consistency is reasoning that style guides exist in the first place.

Each programming language and project will most likely already have a style guide they wish for you to use. The most important aspect of any style guide is to stay consistent. If you wish to work on another project, you should use the existing style guide. If you don't... they probably won't like you very much. Conforming to an existing style guide is often made simpler by installing a linter. Many programming languages have existing linters that you can run your code through, or add to your IDE, which will automatically handle formatting your code to fit their style guide.

<h2 id="Readability">Readability</h2>

The code should prioritize readability. This means that it should be easy for you and other maintainers to understand, modify, and maintain. This should be facilitated through a mixture of naming conventions, structured programming, comments, and a prioritization of consistency.

<h2 id="Headers">Header Comment</h2>

A header comment, a comment at the beginning of the code, is useful in tracking details such as the license the code uses, the author of the code, and when the code was created.

You could also add a small description about what the project does and/or what the file does. However, this could become verbose very quickly.

An example of what a header comment could look like is:

---

Project: [Project Name] [(link to website, source code, or repository)].

Copyright: Copyright (c) [First Year]-[Current Year] [Project Name] Contributors

Version: [Version Number]

Status: [Removed, Deprecated, Prototype, Development, Production]

License: [License]

Author(s): [Author - Contact,]

Maintainer: [Author - Contact]

Credit: [Credit to additional parties that aren't contributors]

Project Description: [Small description about what this project does]

File Description: [Small description about what this file does]

---

This header comment is very verbose. Feel free to pick and choose the elements to use in your header comment at your discretion. The only ones you truly need to include are the ones required by the license you're using.

<h2 id="Footers">Footer Comment</h2>

A footer comment, a comment at the end of the code, is used to track the contributions of contributors. This is used to keep track of changes to the code in the event that the source control system fails or is removed.

An example footer comment would look like:

---

History of Contributions:
[Year/Month/Day] - [Author - Contact] - [Brief description of the change]
...

---

With each contribution being listed below.

This is an optional element to include in your code that. It is an element that I have never seen included in another style guide, but I feel it could be useful. Possibly, to prevent it from becoming too verbose would be record a date range instead of a single date. That way not every contribution needs to be listed, only large changes of note.

<h2 id="Comments">Comments</h2>

You will find many who will say things along the lines of "code should be self-documenting." I do not agree. I believe that code should have as many comments as needed. What many would probably consider too many comments. Code should be "self-documenting" in the sense that naming conventions, structured programming, consistency, etc. However, I believe that very rarely will a comment truly deter much readability. In contrary a comment will more often than not add insight into the code itself or the programmer's reasoning or mindset. What may be clear in the code to you now may not be in a month, year, or even a day. The code may also not be clear to the next maintainer or user of the codebase. For these reasons I believe that comments should be used extensively.

The verbosity of the comments is up to the discretion of the programmer. However, I believe a good rule of thumb is that whenever you are stumped or confused you should add a comment. If you as the one creating it are confused, it is rationale to assume that the next maintainer, or even you at a future date, would be confused or stumped as well.

Ideally a good comment describes why you're doing something.

Classes, structures, etc. should be given a comment describing what it does. This comment can also include a section describing variables, arguments, parameters, attributes, etc. Examples of how they could be implemented or used could also be beneficial.

Functions can be given comments describing them similarly to Classes, structures, etc., but not every function will be complex enough to need such a comment.

Variables can be given comments if you feel that they're needed.

Comments for control flow such as conditional statements, loops, etc. should be handled as needed.

It could prove helpful to develop types of comments to keep standardized as well. For example, you could have a "TODO" or "FIX" type of comment used to easily search for code that is temporary or needs to be addressed.

Another example could be "Author: Name - Contact" to specify sections of code worked on by specific authors, as well as "Year: YYYY" or "Date: YYYY/MM/DD" to track when the code was worked on. I personally believe that this information should be recorded in the source code. In the event of the source control system failing, having the author and date information about sections of code in the source code directly would maintain credit.

Comments **need** to be updated to be consistent with any changes that occur to the code itself. The only truly bad comment, in my opinion, is one that is not accurate.

Overall, my philosophy when it comes to comments is to use them as much as you need, think you need, or think you may need in the future, and to provide as much verbosity are you see fit.

<h2 id="Documentation">Documentation</h2>

You should always try and create documentation for what you're creating. Especially, if you expect others to use it. For your own sanity it is best to create some kind of documentation. If you don't at some point in the future, you will revisit your code and wish you had.

How verbose and complex or brief and simple you make this documentation is up to you. Whatever format you decide to use for your documentation is up to you as well. It should be in a format that is easily accessible and modifiable by other developers.

<h2 id="Naming_Conventions">Naming Conventions</h2>

There are 4 common naming conventions:

- snake_case
- camelCase
- PascalCase
- kebab-case

In addition to the above naming conventions there is Hungarian notation. This is a type of notation where data type information is added to the name of a function, variable, etc. usually as a prefix. Hungarian notation is not often used anymore due to IDEs displaying variable types but can be used if desired.

The following are the naming conventions you should use for different elements:

- Namespace: 1-word (lowercase)
- Module: 1-word (lowercase)
- Package: 1-word (lowercase)

---

- Class: PascalCase
- Class Member: snake_case (lowercase)

---

- Struct: PascalCase
- Struct Member: snake_case (lowercase)

---

- Enum: PascalCase
- Enum Member: snake_case (lowercase)

---

- Type: PascalCase

---

- Interface: PascalCase

---

- Template: PascalCase

---

- Macro: SNAKE_CASE (Capital)

---

- Function: camelCase
- Method: camelCase

---

- Variable: snake_case (lowercase)

---

- Constant: SNAKE_CASE (Capital)

---

- File Name: kebab-case or snake_case (lowercase, with hyphens used sparingly)
- Directory/Folder Name: kebab-case or snake_case (lowercase, with hyphens used sparingly)
- URL: kebab-case

---

- Database Table/Collection: snake_case (Singular not plural, but this is mostly a personal choice just stay consistent)
- Database Columns/Field: snake_case (Singular)
- Primary Key: snake_case (Ex: table_id)
- Foreign Key: snake_case (Keep the name consistent across tables)

<h2 id="Naming_Rules">Naming Rules</h2>

Names that you use should be readable and clear to what they do.

You should use names that describe the purpose, intent, or use of the object being named. Abbreviations should not be used, unless it would be known by outside observers. The quality of the name should be prioritized over shortening the length of the name.

What you name objects is up to your discretion but be consistent and descriptive. The object's purpose should be easily readable from their given name. The objects name should also follow the Naming Conventions for the type of object it is.

<h2 id="Exception_Handling">Exception Handling</h2>

Exception handling should be used sparingly. Exception handling should be used when there's a possible error. You have the option of either trying to recover from the error or to throw an exception and give the user information about the error that occurred.

A common use for exception handling is when you get inputs. These inputs may not be valid. You can use exception handling to inform the user to format their inputs in the expected way. Another common example is when attempting to open a file that may or may not exist.

<h2 id="Max_Line_Length">Maximum Line Length</h2>

A good max line length is 80 characters. However, set this to what looks best to you and keep it consistent.

<h2 id="Blank_Lines">Blank Lines</h2>

Blank lines should be used to separate different elements and blocks in the code.

Functions should be separated from other functions and elements with a single blank line.

Classes, structures, etc. should be separated from other functions and elements by two blank lines.

Blocks of code, sections of code related to each other, should be separated from other blocks of code by a single blank line.

Comments should not be separated with blank lines. Comments should either be inline or directly above or below another element. The only exception being comments that are not directly related to what is above or below them. Such as describing the general though process of the surrounding code, not the code itself.

<h2 id="Indentation">Indentation</h2>

The most common indentation sizes are 4 and 2 spaces. 4 spaces per indentation is the common default size used by many IDES. Choose the size you prefer and be consistent. Every IDE should transform the tab key into spaces. Don't be a maniac who is manually entering spaces every indentation. You can install a linter and let it handle making this consistent for you.

<h2 id="Curly_Bracket">Curly Brackets</h2>

If the programming language you're using uses curly brackets, or another symbol, to start and end code blocks there is always a debate. Do I put them on the same line or the next line? This is a personal preference.

For this style guide put the curly brackets on the same line.

<h2 id="Parentheses">Parentheses</h2>

Parentheses are used to handle the order of operations or order of evaluation, handle expressions, and invoke functions in programming languages.

However, some programming languages require parentheses around certain expressions. For example, R, C++, and JavaScript require parentheses around conditional statements, but Python and don't require them. This is another decision that should be handled by the general community standard of the programming language. Personally, I'm biased to put parentheses around conditional statements, but the Python general community consensus is to not use parentheses.

<h2 id="Semicolon">Semicolon</h2>

In most programming languages the semicolon serves the purpose of ending a statement. However, not every programming language uses a semicolon as the symbol to end a statement. Consider this section regarding whatever the symbol ending a statement is in your current programming language is.

In most programming languages using a semicolon isn't a choice. If you're ending a statement you need to use one. However, there are programming languages such as Python and JavaScript that support semicolons but aren't required. If you're using a programming language where they're not required, you should follow the standard guide of that programming language. For example, in JavaScript you should be using semicolons, but in Python you should never use a semicolon.

<h2 id="Quotes">Quotes</h2>

Should you use single or double quotes? Maybe the programming language you're using supports backticks. Depending on the programming language you're using there may be special definitions for these symbols. In many languages single quotes are a char and double quotes are a string. However, in many languages single and double quotes are interchangeably. You should use whichever choice is better for the programming language you're using.

If you're using C++ use double quotes, if you're using Python use f-strings with either single or double quotes, if you're using JavaScript use backticks, and if you're using R use double quotes. It depends on the programming language and you're personal preference. For example, in Python, R, and JavaScript single and double quotes do the same thing.

Using a single quote will be seen as more efficient by some because you don't need to press shift. However, programmers who come from languages like C, C++, C#, and Java, which have the char data type, will be used to using the double quote for strings out of habit.

In programming languages that don't have the char data type you should use single quotes for strings, but for programming languages with the char data type you should use double quotes.

<h2 id="Max_Nesting_Levels">Max Nesting Levels</h2>

Nesting is when you write a block of code inside of another block of code.

In most programming languages you will probably be able to nest code more times than you could ever possibly write. However, because you can do something doesn't mean you should. The main reason is due to preserving the readability of the code. With every level of nesting, you add the code can become less readable and confusing.

In most circumstances you shouldn't be using more than 3 nesting levels from the "root" level, the initial block of code.

More nesting levels can be used, but you're already limited in part by the size of the indentation and the line width. After a certain point there's not enough space for any readability, which is why you should limit the amount of nesting you use. The most common way to reduce the amount of nesting needed is to refactor your code into separate functions.

Operators, if following directions, should be left-handed. For example, if defining a variable with assignment and/or declaration you should have the variable name on the left and the value on the right.

<h2 id="Optimization">Optimization</h2>

You should aim to make your code as optimized as you are capable of achieving.

We live in a time where computers are more than capable of running even the most unoptimized code, inefficient code, poorly written code, and slow programming languages at speeds faster than you could ever reasonably need. However, I believe you should still aim to create the highest quality product that you are capable of. To not strive to create the best work you can is a disservice to yourself as a creator.

<h2 id="PLP">Principle of Least Privilege</h2>

You should use the least amount of privilege possible for your application. Meaning that you should use as little permissions, resources, data, and other applications as required by your application.

<h2 id="PLA"> General Programming Language Information</h2>

Programming languages are statically typed or dynamically typed. Statically typed programming languages need variables to be assigned a data type and are checked at compile time, while dynamically typed programming languages do not require variables to be assigned data types and are checked during execution or runtime. Statically types programming languages require you to explicitly assign a data type, while a dynamically typed programming language will assign the data type for you. You also can't change or convert the data type of a variable after it's been created in a statically typed programming language, but you can in a dynamically typed programming language.

Programming languages are also strongly typed or weakly typed. Strongly typed programming languages have strict rules and constraints when it comes to what you can do with a data type. Weakly typed programming languages have loose rules and constraints about what you can do with a data type. The definitions of strong and weak typing are still controversial and not agreed upon. However, generally the consensus seems that a strongly typed programming language won't allow implicit conversion while a weakly typed programming language will. Implicit conversion allows a data type to be transformed from one data type to another automatically. While explicit conversion only allows for data types to be transformed to another data type when explicitly told to, such as by being cast.

---

Programming languages are also either compiled or interpreted.

Compiled programming languages are run through a compiler to transform source code into machine code or object code. This resulting machine or object code is run natively on the platform or the runtime environment it was compiled for. There are two main types of compiled programming languages Ahead of Time and Just in Time. Ahead of Time compilers are compiled statically, before the program is running, and Just in Time compilers are compiled dynamically, while the program is running.

Interpreted programming languages are run the source code through an interpreter. The interpreter itself runs on the native platform and executes the source code. The difference between an interpreter and a Just in Time compiler is that an interpreter will read and execute code as it goes, while a Just in Time compiler will read and compile to machine code or object code the parts it needs as it needs it.

Some programming languages are compiled to another form of code known as bytecode or an intermediate language, which is then run through an interpreter or even a Just in Time compiler. Such as Java which compiles its source code into bytecode and then runs it through its interpreter and Just in Time compiler the JVM.

Some compilers will go through an intermediate step of generating assembly or provide the option to generate assembly instead of machine code. This assembly would then get sent through an assembler to create the machine code.

Compiled programming languages are often much faster in terms of execution than interpreted programming languages, but you have to compile them for every platform you use. Interpreted programming languages may be slower but have more flexibility because you can run the source code directly on any platform given that you have an interpreter for it.

---

Programming languages are either high-level or low-level. High-level programming languages are separated highly from the underlying machine code and are very human-readable, but not machine-readable Low-level programming languages are much closer to the underlying machine code and are not very human-readable but are much more machine-readable. High-level programming languages are very portable and can be used on various platforms, but they need to be compiled or interpreted. Low-level programming languages are not very portable and can only be used on the platform they're built for; they need to be assembled. Some high-level programming languages are C, C++, C#, Java, Python, R, and Javascript. Low-level programming languages consist of machine code itself and the different types of assembly built for specific instruction set architecture, computer architecture, platforms, or processors. Assembly is the lowest level of human-readable programming languages and is very strongly related to a computer architecture's instructions.

---

Variables in most programming languages have 2 general scopes: local and global. Variables in the global scope are accessible from anywhere in the code. Variables in the local scope are only accessible withing the block of code they're defined in.

---

Many object-oriented programming languages have access modifiers. Access modifiers are used to restrict access to class members. Different programming languages will have different access modifiers. I will use the access modifiers from C# instead of C++ or Java, because C# has the most.

- Public: Access isn't restricted.
- Private:  Accessible to the containing class.
- Protected: Accessible to the containing class or derived (inherited) classes.
- Internal: Accessible to the current assembly (executables and libraries).
- File: Only accessible to the current source file.
- Protected Internal: Accessible to the current assembly (executables and libraries) or derived (inherited) classes.
- Private Protected: Accessible to the containing class or derived (inherited) classes within the current assembly (executables and libraries).
