# Garrett's General Programming Style Guide

# Table of Contents

- [Readability](#Readability)
- [Headers](#Headers)
- [Footers](#Footers)
- [Comments](#Comments)
- [Documentation](#Documentation)
- [Naming Conventions](#Naming_Conventions)
- [Variables](#Variables)
- [Functions](#Functions)
- [Classes](#Classes)
- [Formatting](#Formatting)
- [Exception Handling](#Exception_Handling)
- [Maximum Line Length](#Max_Line_Length)
- [Blank Lines](#Blank_Lines)
- [Indentation](#Indentation)
- [Code Blocks](#Code_Blocks)
- [Max Nesting Levels](#Max_Nesting_Levels)
- [Operators](#Operators)
- [Iterators](#Iterators)
- [Containers](#Containers)
- [Optimization](#Optimization)

---

# Preamble

This document serves as a general style guide to be used across various programming languages. This is a style guide that I am creating for myself. The most important part of this style guide will be the naming conventions, as these will stay consistent across most languages. Other aspects regarding to syntax and such can change depending on the language. If you decide to use this style guide feel free to modify it in anyway that makes your code more consistent. Consistency is reason that style guides exist in the first place.

 Each programming language and project will most likely already have a style guide they wish for you to use.  The most important aspect of any style guide is to stay consistent. If you wish to work with another project you should use the existing style guide. If you don't... they probably won't like you very much. Conforming to an existing style guide is often made simpler by installing a linter. Many programming languages have existing linters that you can run your code through, or add to your IDE, that will automatically handle formatting your code to fit their style guide.

<h2 id="Readability">Readability</h2>

<h2 id="Headers">Headers</h2>

<h2 id="Footers">Footers</h2>

<h2 id="Comments">Comments</h2>

<h2 id="Documentation">Documentation</h2>

You should always try and create documentation for what you're creating. Especially, if you expect others to use it. For your own sanity it is best to create some kind of documentation. If you don't at some point in the future, you will revisit your code and wish you had.

How verbose and complex or brief and simple you make this documentation is up to you. Whatever format you decide to use for your documentation is up to you as well. It should be in a format that is easily accessible and modifiable by other developers.

<h2 id="Naming_Conventions">Naming Conventions</h2>

There are 4 common naming conventions:

- snake_case
- camelCase
- PascalCase
- kebab-case

In addition to the above naming conventions there is Hungarian notation. This is a type of notation where data type information is added to the name of a function, variable, etc. usually as a prefix. Hungarian notation is not often used anymore due to IDEs displaying variable types, but can be used if desired.

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

<h2 id="Variables">Variables</h2>

<h2 id="Functions">Functions</h2>

<h2 id="Classes">Classes</h2>

<h2 id="Formatting">Formatting</h2>

<h2 id="Exception_Handling">Exception Handling</h2>

<h2 id="Max_Line_Length">Maximum Line Length</h2>

A good max line length is 80 characters. However, set this to what looks best to you and keep it consistent.

<h2 id="Blank_Lines">Blank Lines</h2>

<h2 id="Indentation">Indentation</h2>

The most common indentation sizes are 4 and 2 spaces. 4 spaces per indentation is the common default size used by many IDES. Choose the size you prefer and be consistent. Every IDE should transform the tab key into spaces. Don't be a maniac who is manually entering spaces every indentation. You can install a linter and let it handle making this consistent for you.

<h2 id="Code_Blocks">Code Blocks</h2>

<h2 id="Max_Nesting_Levels">Max Nesting Levels</h2>

<h2 id="Iterators">Iterators</h2>

<h2 id="Operators">Operators</h2>

<h2 id="Containers">Containers</h2>

<h2 id="Optimization">Optimization</h2>
