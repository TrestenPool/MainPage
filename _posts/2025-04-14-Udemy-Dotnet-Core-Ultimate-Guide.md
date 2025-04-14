---
layout: post
title: "Udemy - .Net Core True Ultimate Guide"
date: 2025-04-14
desc: "this is the description"
categories: [Dotnet]
tags: [Udemy]
icon: icon-csharp
---

- [About](#about)
- [Chapter 17 - Tag Helpers](#chapter-17---tag-helpers)
  - [About Tag Helpers](#about-tag-helpers)
  - [Importing Tag Helpers](#importing-tag-helpers)
  - [Form Tag Helpers](#form-tag-helpers)
  - [Input Tag Helpers](#input-tag-helpers)
  - [Adding datatype to the Model](#adding-datatype-to-the-model)


# About
---

  Notes from the following Udemy course
  - [Udemy Course Link](https://www.udemy.com/course/asp-net-core-true-ultimate-guide-real-project/)

---
<br><br>

# Chapter 17 - Tag Helpers
<br>

## About Tag Helpers
---

What are tag helpers
  - classes that can be invoked as an html tag or an html attribute

Example
  - `<input aspfor="ModelProperty">`
  - gets transformed into 
  - `<input type="text" name="ModelProperty" id="ModelProperty" value="ModelValue">`

Predefined Tag helpers for `<a> <form>`
  - asp-controller
  - asp-action
  - asp-route-x
  - asp-route
  - asp-area

Predefined Tag helpers for `<input> <textarea>, <label>`
  - asp-for

Predefined Tag helpers for `<select>`
  - asp-for
  - asp-items

---
<br><br>

## Importing Tag Helpers
---

How to import
  - In order to use the predefined tag helpers you must first import them
  - The following snippet of code is conventionally put in the **_ViewImports.cshtml** file in razor & MVC 
  - The structure is `@addTaghelper * {DLL_NAME}`
  - `@addTagHelper *, Microsoft.AspNetCore.MVC.TagHelpers`
  
---
<br><br>

## Form Tag Helpers
---

This is a regular anchor tag

`<a href="~/persons/index" class="link-hover">Back to persons index page</a>`

This is an anchor tag with the tag helpers **asp-controller** and **asp-action**<br>

`<a asp-controller="Persons" asp-action="Index" class="link-hover">Back to index page</a>`

---
<br><br>

## Input Tag Helpers
---

`<input asp-for="ModelProperty />"`

is equivalient to ...

`<input type="text" name="ModelProperty" id="ModelProperty" value="ModelValue" data-val-rule="ErrorMessage" />`



---
<br><br>

## Adding datatype to the Model
---

```
Hello world
```

---
<br><br>