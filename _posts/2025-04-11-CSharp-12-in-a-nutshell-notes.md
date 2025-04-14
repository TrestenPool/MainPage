---
layout: post
title: "C# 12 In A Nutshell"
date: 2025-04-11
desc: "this is the description"
categories: [Csharp]
tags: [C#, Book]
icon: icon-csharp
---

- [About](#about)
- [Chapter 3 (Creating types in C#)](#chapter-3-creating-types-in-c)
  - [Interfaces](#interfaces)
    - [Explicit Interface Implementation](#explicit-interface-implementation)


# About
---

  - This blog entry just goes over all of the things I found interesting and wanted to take note of when reading **C# 12 in a nutshell**

---
<br><br>


# Chapter 3 (Creating types in C#)
---

## Interfaces

### Explicit Interface Implementation
C# allows you to explicitly allow some methods to only be called when you cast to the interface you are coding to.
```
  interface I1 {
    void mymethod();
  }

  interface I2 {
    void mymethod();
  }

  public class SubClass : I1, I2{
    void I1.mymethod(){
      Console.WriteLine("i1 mymethod");
    }
    void I2.mymethod(){
      Console.WriteLine("i2 mymethod");
    }
  }
```
- for example take these two interfaces that define the **mymethod**
- The **Subclass** implements both interfaces

In the main method we have the following code
```
  SubClass subClass = new();

  // output: i1 mymethod
  ((I1)subClass).mymethod();

  // output: i2 mymethod
  ((I2)subClass).mymethod();
  
  // compile time error
  subClass.mymethod();
```
- we have to **cast** to the interface to get the method to work, otherwise omitting we will get a **compile time error**

Use Cases
  - can be used to hide members that are highly specialized and distracting to a types normal use case
    - For example a type that implements ISerializable would typically want to avoid showing those methods to the user

---
<br><br>
