---
layout: post
title: "What happens under the hood in .NET Core"
date: 2025-04-14
desc: "this is the description"
categories: [Dotnet]
tags: [Dotnet]
icon: icon-csharp
---

# What happens at Startup
--- 

<br>

1. Project Building
  - .net sdk reads the .csproj file
  - It resolves and downloads (if not already present in the NuGet cache) all the NuGet packages specified as dependencies in the .csproj file.
  - The C# compiler (csc.exe) compiles the .cs files (Program.cs, Startup.cs, etc.) into Intermediate Language (IL) code.
  - The IL code, along with the project's dependencies, is assembled into an assembly (typically a .dll file)
  
2. Host Builder Initialization
  - The execution starts in the Main method of the Program.cs file.
  - The code in Program.cs typically sets up a host builder (WebHost.CreateDefaultBuilder(args) or Host.CreateDefaultBuilder(args) in newer versions). The host is responsible for managing the application's lifecycle and providing essential services.




