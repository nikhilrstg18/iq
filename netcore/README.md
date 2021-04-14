# .Net Core Interview Questions & Answers 🌹 [![GitHub](https://img.shields.io/github/license/nikhilrstg18/iq?color=blue)](https://github.com/nikhilrstg18/iq/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/nikhilrstg18/iq) ![GitHub forks](https://img.shields.io/github/forks/nikhilrstg18/iq)

> Click :star: if you like the project. Pull Requests are highly appreciated.

> [![Twitter](https://img.shields.io/twitter/follow/rustagi_nikhil?label=Follow%20%40rustagi_nikhil&style=social)](https://twitter.com/rustagi_nikhil) for technical updates.

---

## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---

### Table of Contents

| No. | Questions                                                                                                                                                                                               |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is .NET core ?](#what-is-.net-core)                                                                                                                                                               |
| 1.1 | [What are some characteristics of .NET Core ?](#what-are-some-characteristics-of-.NET-Core)                                                                                                             |
| 1.2 | [Explain what is included in .NET Core ?](#explain-what-is-included-in-.NET-Core)                                                                                                                       |
| 1.3 | [.NET Core Vs Mono ?](#.NET-Core-Vs-Mono)                                                                                                                                                               |
| 2   | [What is .NET Framework?](#what-is-.net-framework)                                                                                                                                                      |
| 3   | [What is .NET Standard and why we need to consider it?](#what-is-.net-standard-and-why-we-need-to-consider-it)                                                                                          |
| 4   | [What is CLR ?](#what-is-clr)                                                                                                                                                                           |
| 4.1 | [Name some Service of CLR.](#Service-of-CLR)                                                                                                                                                            |
| 4.2 | [Name some Benefits of CLR.](#Benefits-of-CLR)                                                                                                                                                          |
| 4.3 | [What is CoreCLR ?](#What-is-CoreCLR)                                                                                                                                                                   |
| 5   | [What is CLS ?](#what-is-cls)                                                                                                                                                                           |
| 6   | [What is CTS ?](#what-is-cts)                                                                                                                                                                           |
| 7   | [What is Garbage Collector ?](#what-is-garbage-collector)                                                                                                                                               |
| 8   | [What is JIT Compiler ?](#what-is-jit-compiler)                                                                                                                                                         |
| 9   | [What is MSIL ?](#what-is-msil)                                                                                                                                                                         |
| 10  | [What is .NET Standard and why we need to consider it ?](#what-is-.net-standard-and-why-we-need-to-consider-it)                                                                                         |
| 11  | [What is a .NET application domain ?](#what-is-a-.net-application-domain)                                                                                                                               |
| 12  | [What's the difference between SDK and Runtime in .NET Core ?](#What's-the-difference-between-SDK-and-Runtime-in-.NET-Core)                                                                             |
| 13  | [What is difference between .NET Core and .NET Framework and Xamarin ?](#What-is-difference-between-.NET-Core-and-.NET-Framework-and-Xamarin)                                                           |
| 14  | [What about NuGet packages and packages.config ?](#What-about-NuGet-packages-and-packages.config)                                                                                                       |
| 15  | [Talk about new .csproj file ?](#Talk-about-new-.csproj-file)                                                                                                                                           |
| 16  | [Explain the difference between “managed” and “unmanaged” code ?](#Explain-the-difference-between-“managed”-and-“unmanaged”-code)                                                                       |
| 17  | [Why to use of the IDisposable interface ?](#Why-to-use-of-the-IDisposable-interface)                                                                                                                   |
| 18  | [Explain the difference between Task and Thread in .NET ?](#Explain-the-difference-between-Task-and-Thread-in-.NET)                                                                                     |
| 19  | [What is Explicit Compilation?](#What-is-Explicit-Compilation?)                                                                                                                                         |
| 20  | [What are the benefits of explicit compilation?](#What-are-the-benefits-of-explicit-compilation?)                                                                                                       |
| 21  | [What is the difference between Class Library (.NET Standard) and Class Library (.NET Core)?](<#What-is-the-difference-between-Class-Library-(.NET-Standard)-and-Class-Library-(.NET-Core)?>)           |
| 22  | [What's is BCL?](#What's-is-BCL?)                                                                                                                                                                       |
| 23  | [When should we use .NET Core and .NET Standard Class Library project types?](#When-should-we-use-.NET-Core-and-.NET-Standard-Class-Library-project-types?)                                             |
| 24  | [What is implicit compilation?](#What-is-implicit-compilation?)                                                                                                                                         |
| 25  | [What is FCL?](#What-is-FCL?)                                                                                                                                                                           |
| 26  | [Does .NET support multiple inheritance?](#Does-.NET-support-multiple-inheritance?)                                                                                                                     |
| 27  | [What is the difference between .NET Framework/Core and .NET Standard Class Library project types?](#What-is-the-difference-between-.NET-Framework/Core-and-.NET-Standard-Class-Library-project-types?) |
| 28  | [What's the difference between RyuJIT and Roslyn?](#What's-the-difference-between-RyuJIT-and-Roslyn?)                                                                                                   |
| 29  | [What is the difference between AppDomain, Assembly, Process, and a Thread?](#What-is-the-difference-between-AppDomain,-Assembly,-Process,-and-a-Thread?)                                               |
| 30  | [What is the difference between CIL and MSIL (IL)?](<#What-is-the-difference-between-CIL-and-MSIL-(IL)?>)                                                                                               |
| 31  | [Why does .NET Standard library exist?](#Why-does-.NET-Standard-library-exist?)                                                                                                                         |
| 32  | [Explain how does Asynchronous tasks (Async/Await) work in .NET?](<#Explain-how-does-Asynchronous-tasks-(Async/Await)-work-in-.NET?>)                                                                   |
| 33  | [Why does .NET use a JIT compiler instead of just compiling the code once on the target machine?](#Why-does-.NET-use-a-JIT-compiler-instead-of-just-compiling-the-code-once-on-the-target-machine?)     |
| 34  | [What are benefits of using JIT?](#What-are-benefits-of-using-JIT?)                                                                                                                                     |
| 35  | [How to choose the target version of .NET Standard library?](#How-to-choose-the-target-version-of-.NET-Standard-library?)                                                                               |
| 36  | [What is the difference between Node.js async model and async/await in .NET?](#What-is-the-difference-between-Node.js-async-model-and-async/await-in-.NET?)                                             |
| 37  | [Explain Finalize vs Dispose usage?](#Explain-Finalize-vs-Dispose-usage?)                                                                                                                               |
| 38  | [How many types of JIT Compilations do you know?](#How-many-types-of-JIT-Compilations-do-you-know?)                                                                                                     |

---

1. ### What is .Net Core

    <img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/netstandard.png" alt=".Net Standard Vs .Net Core Vs .Net Framework" width=600px />

   The [.NET Core](https://dotnet.microsoft.com/download) platform is a new .NET stack that is optimized for open source development and agile delivery on NuGet.

   .NET Core has two major components. It includes a small runtime that is built from the same codebase as the .NET Framework CLR. The .NET Core runtime includes the same **GC** and **JIT** (RyuJIT), but doesn’t include features like Application Domains or Code Access Security. The runtime is delivered via NuGet, as part of the ASP.NET Core package.

   .NET Core also includes the base class libraries **(BCL)**. These libraries are largely the same code as the .NET Framework class libraries, but have been factored (removal of dependencies) to enable to ship a smaller set of libraries. These libraries are shipped as `System.*` NuGet packages on [nuget.org](https://www.nuget.org/)

   > #### What are some characteristics of .NET Core ?

   - Flexible deployment: Can be included in your app or installed side-by-side user- or machine-wide.

   - Cross-platform: Runs on Windows, macOS and Linux; can be ported to other OSes. The supported Operating Systems (OS), CPUs and application scenarios will grow over time, provided by Microsoft, other companies, and individuals.

   - Command-line tools: All product scenarios can be exercised at the command-line.

   - Compatible: .NET Core is compatible with .NET Framework, Xamarin and Mono, via the .NET Standard Library.

   - Open source: The .NET Core platform is open source, using MIT and Apache 2 licenses. Documentation is licensed under CC-BY. .NET Core is a .NET Foundation project.

   - Supported by Microsoft: .NET Core is supported by Microsoft, per .NET Core Support

   > #### Explain what is included in .NET Core

   - A .NET runtime, which provides a type system, assembly loading, a garbage collector, native interop and other basic services.

   - A set of framework libraries, which provide primitive data types, app composition types and fundamental utilities.

   - A set of SDK tools and language compilers that enable the base developer experience, available in the .NET Core SDK.

   - The 'dotnet' app host, which is used to launch .NET Core apps. It selects the runtime and hosts the runtime, provides an assembly loading policy and launches the app. The same host is also used to launch SDK tools in much the same way.

   > #### .NET Core Vs Mono

   - Mono is third party implementation of .Net Framework for Linux/Android/iOs

   - .Net Core is Microsoft's own implementation for same.

   **[⬆ Back to Top](#table-of-contents)**

---

2. ### What is .NET Framework

   The .NET is a Framework, which is a `collection of classes of reusable libraries given by Microsoft to be used in other` .NET applications and to develop, build and deploy many types of applications on the Windows platform including the following:

   - `Console` Applications
   - `Windows Forms` Applications
   - `Windows Presentation Foundation` (WPF) Applications
   - `Web Applications`
   - `Web Services`
   - `Windows Services`
   - Services-oriented applications using `Windows Communications Foundation` (WCF)
   - Workflow-enabled applications using `Windows Workflow Foundation` (WF)

   **[⬆ Back to Top](#table-of-contents)**

---

3. ### What is .NET Standard and why we need to consider it

   **.NET Standard**

   > is a formal specification of .NET APIs that are intended to be available on all .NET implementations

   or

   > is a set of APIs that all .NET platforms have to implement.

   This unifies the .NET platforms and prevents future fragmentation.

   - **.NET Standard** solves the code sharing problem for .NET developers across all platforms by bringing all the APIs that you expect and love across the environments that you need: desktop applications, mobile apps & games, and cloud services:
   - **.NET Standard** 2.0 will be implemented by .NET Framework, .NET Core, and Xamarin. For .NET Core, this will add many of the existing APIs that have been requested.
   - **.NET Standard** 2.0 includes a compatibility shim for .NET Framework binaries, significantly increasing the set of libraries that you can reference from your **.NET Standard** libraries.
   - **.NET Standard** will replace Portable Class Libraries (PCLs) as the tooling story for building multi-platform .NET libraries

   **[⬆ Back to Top](#table-of-contents)**

---

4. ### What is CLR

   The CLR stands for `Common Language Runtime` and it is an Runtime Environment in .Net.

   <img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/clr.png" alt="Illustration level at which CLR operates" width=400px height=350px/>

   Main components of CLR:

   - **Common Language Specification** (**CLS**)
   - **Common Type System** (**CTS**)
   - **Garbage Collection** (**GC**)
   - **Just In – Time** Compiler (**JIT**)

   It works as a layer between Operating Systems and the applications written in .NET languages that conforms to the Common Language Specification (CLS).

   The main function of Common Language Runtime (CLR) is to convert the Managed Code into native code and then execute the program.

   > #### Service of CLR:

   - Assembly Resolver
   - Assembly Loader
   - Type Checker
   - COM marshalled
   - Debug Manager
   - Thread Support
   - IL to Native compiler
   - Exception Manager
   - Garbage Collector

   > #### Benefits of CLR:

   - It improves the performance by providing a rich interact between programs at run time.
   - Support automatic memory management with the help of Garbage Collector.
   - Enhance portability by removing the need of recompiling a program on any operating system that supports it.
   - Provide language, platform, and architecture independence.
   - Security also increases as it analyzes the MSIL instructions whether they are safe or unsafe. Also, the use of delegates in place of function pointers enhance the type safety and security.
   - Provides cross-language integration because CTS inside CLR provides a common standard that activates the different languages to extend and share each other’s libraries.
   - Provides support to use the components that developed in other .NET programming languages.
   - It allows easy creation of scalable and multithreaded applications, as the developer has no need to think about the memory management and security issues.

   > #### What is CoreCLR
   >
   > CoreCLR is the .NET execution engine in .NET Core, performing functions such as garbage collection and compilation to machine code

   **[⬆ Back to Top](#table-of-contents)**

---

5. ### What is CLS

   It is responsible for converting the different .NET programming language syntactical rules and regulations into CLR understandable format. Basically, it provides the Language Interoperability. Language Interoperability means to provide the execution support to other programming languages also in .NET framework.

   `Language Interoperability` can be achieved in two ways :

   > **Managed Code**:

   - The `MSIL` code which is managed by the `CLR` is known as the `Managed Code`. For managed code CLR provides three .NET facilities:
     - **CAS** (Code Access Security)
     - Exception Handling
     - Automatic Memory Management.\

   > **Unmanaged Code**:

   - Before .NET development the programming language like .COM Components & Win32 API do not generate the MSIL code. So these are not managed by `CLR` rather managed by Operating System.\
   - Anything you've used P/Invoke calls to get outside of the nice comfy world of everything available to you in the .NET Framwork is unmanaged – and you're now responsible for cleaning it up

   **[⬆ Back to Top](#table-of-contents)**

---

6. ### What is CTS

   Every programming language has its own data type system, so CTS is responsible for understanding all the data type systems of .NET programming languages and converting them into CLR understandable format which will be a common format.

   There are 2 Types of CTS that every .NET programming language have :

   > **Value Types**:

   Value Types will `store the value directly into the memory location`.\
    These types work with stack mechanism only.\
    CLR allows memory for these at Compile Time.

   > **Reference Types**:

   Reference Types will `contain a memory address of value because the reference types won’t store the variable value directly in memory`. \
    These types work with Heap mechanism.\
    CLR allots memory for these at Runtime.

   **[⬆ Back to Top](#table-of-contents)**

---

7. ### What is Garbage Collector

   It is used to provide the Automatic Memory Management feature. \
    If there was no garbage collector, programmers would have to write the memory management codes which will be a kind of overhead on programmers.

   **[⬆ Back to Top](#table-of-contents)**

---

8. ### What is JIT Compiler

   JIT stands for **Just In Time**. \
    It is responsible for converting the `MSIL` or `CIL`(Common Intermediate Language) into machine code or native code using the `Common Language Runtime` environment.

   Before a computer can execute the source code, special programs called compilers must rewrite it into machine instructions, also known as object code. This process (commonly referred to simply as “compilation”) can be done explicitly or implicitly.

   Implicit compilation is a two-step process:

   - The first step is converting the source code to intermediate language (IL) by a language-specific compiler.
   - The second step is converting the IL to machine instructions. The main difference with the explicit compilers is that only executed fragments of IL code are compiled into machine instructions, at runtime. The .NET framework calls this compiler the JIT (Just-In-Time) compiler.

   **[⬆ Back to Top](#table-of-contents)**

---

9. ### What is MSIL or CIL

   When we compile our .NET code then it is not directly converted to native/binary code; it is first converted into intermediate code known as MSIL code which is then interpreted by the CLR. MSIL is independent of hardware and the operating system. Cross language relationships are possible since MSIL is the same for all .NET languages. MSIL is further converted into native code.

   **[⬆ Back to Top](#table-of-contents)**

---

10. ### What is a .NET application domain

It is an isolation layer provided by the .NET runtime. As such, App domains live with in a process (1 process can have many app domains) and have their own virtual address space.

App domains are useful because:

- They are less expensive than full processes
- They are multithreaded
- You can stop one without killing everything in the process
- Segregation of resources/config/etc
- Each app domain runs on its own security level

**[⬆ Back to Top](#table-of-contents)**

---

11. ### What is the difference between decimal, float and double in .NET

    When would someone use one of these?

    Precision is the main difference.

    - Float - 7 digits (**32 bit**)
    - Double-15-16 digits (**64 bit**)
    - Decimal -28-29 significant digits (**128 bit**)

    As for what to use when:

    - For values which are "naturally exact decimals" it's good to use decimal. This is usually suitable for any concepts invented by humans: financial values are the most obvious example, but there are others too.

      > Consider the score given to divers or ice skaters, for example.

    - For values which are more artefacts of nature which can't really be measured exactly anyway, float/double are more appropriate.
      > For example, scientific data would usually be represented in this form. Here, the original values won't be "decimally accurate" to start with, so it's not important for the expected results to maintain the "decimal accuracy". Floating binary point types are much faster to work with than decimals.

**[⬆ Back to Top](#table-of-contents)**

---

12. ### What's the difference between SDK and Runtime in .NET Core

    > The **SDK** is all of the stuff that is needed/makes developing a .NET Core application easier, such as the CLI and a compiler.

    > The **runtime** is the "virtual machine" that hosts/runs the application and abstracts all the interaction with the base operating system.

**[⬆ Back to Top](#table-of-contents)**

---

13. ### What is difference between .NET Core and .NET Framework and Xamarin

    .NET as whole now has 2 flavors:

    - **.NET Framework**
    - **.NET Core**

    **.NET Core** and the **.NET Framework** have (for the most part) a subset-superset relationship.

    **.NET Core** is named “Core” since it contains the core features from the **.NET Framework**, for both the runtime and framework libraries.

    > For example, **.NET Core** and the **.NET Framework** share the GC, the JIT and types such as String and List.

    **.NET Core** was created so that .NET could be open source, cross platform and be used in more resource-constrained environments.

    **Xamarin** is used for building mobile apps that can run on iOS, Android, or Windows Phone devices

**[⬆ Back to Top](#table-of-contents)**

---

14. ### What about NuGet packages and packages.config

    There is no more packages.config file. All packages are now managed within .csproj file.

    The .csproj file has been cleaned up and it also serves the role of packages.config(or package.json for Node devs). That means that’s where your packages and versions will be saved.

    NuGet packages are the unit of reference and they can depend on other NuGet packages, but also they can depend on projects. And as before, projects can also depend on NuGet packages and other projects. That means that projects and NuGet packages are interchangeable.

    With .NET Core, you can easily turn your projects into NuGet packages, with one click inside of the properties.

**[⬆ Back to Top](#table-of-contents)**

---

15. ### Talk about new .csproj file

    `.csproj` file is now used as a place where we manage the NuGet packages for your application.

    ```xml
    <Project Sdk="Microsoft.NET.Sdk.Web">

    <PropertyGroup>
        <TargetFramework>net5.0</TargetFramework>
        <CopyRefAssembliesToPublishDirectory>false</CopyRefAssembliesToPublishDirectory>
    </PropertyGroup>

    <ItemGroup>
        <PackageReference Include="Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation" Version="5.0.3" />
    </ItemGroup>

    <ItemGroup>
        <ProjectReference Include="..\GettingStartedWebApp.Data\GettingStartedWebApp.Data.csproj" />
    </ItemGroup>

    </Project>
    ```

    File explorer and project explorer are now in sync. For .NET Core projects, you can easily drop a file from file explorer into a project or delete it from the file system and it will be gone from the project. No more source files in a .csproj file.

    You can now edit the .csproj file directly without unloading the project.

**[⬆ Back to Top](#table-of-contents)**

---

16. ### Explain the difference between “managed” and “unmanaged” code

    > Managed Code

    - is not compiled to machine code but to an intermediate language which is interpreted and executed by some service on a machine and is therefore operating within a (hopefully!) secure framework which handles dangerous things like memory and threads for you.
    - It runs on the **CLR** (Common Language Runtime), which, among other things, offers services like garbage collection, run-time type checking, and reference checking.
    - So, think of it as, "My code is managed by the CLR."

    > Unmanaged code

    - is compiled to machine code and therefore executed by the OS directly.
    - It therefore has the ability to do damaging/powerful things Managed code does not.
    - This is how everything used to work, so typically it's associated with old stuff like .dlls

**[⬆ Back to Top](#table-of-contents)**

---

17. ### Why to use of the IDisposable interface

    The "primary" use of the IDisposable interface is to clean up unmanaged resources.

    Note the purpose of the Dispose pattern is to provide a mechanism to clean up both managed and unmanaged resources and when that occurs depends on how the Dispose method is being called.

**[⬆ Back to Top](#table-of-contents)**

---

18. ### Explain the difference between Task and Thread in .NET

    > Thread

    - Represents an actual OS-level thread, with its own stack and kernel resources.
    - Thread allows the highest degree of control; you can Abort() or Suspend() or Resume() a thread, you can observe its state, and you can set thread-level properties like the stack size, apartment state, or culture.
    - ThreadPool is a wrapper around a pool of threads maintained by the CLR.

    > Task class

    - from the Task Parallel Library offers the best of both worlds.
    - Like the ThreadPool, a task does not create its own OS thread. Instead, tasks are executed by a TaskScheduler; the default scheduler simply runs on the ThreadPool.
    - Unlike the ThreadPool, Task also allows you to find out when it finishes, and (via the generic Task) to return a result.

**[⬆ Back to Top](#table-of-contents)**

---

### What is Explicit Compilation?

---

### What are the benefits of explicit compilation?

---

### What is the difference between Class Library (.NET Standard) and Class Library (.NET Core)?

---

### What's is BCL?

---

### When should we use .NET Core and .NET Standard Class Library project types?

---

### What is implicit compilation?

---

### What is FCL?

---

### Does .NET support multiple inheritance?

---

### What is the difference between .NET Framework/Core and .NET Standard Class Library project types?

---

### What's the difference between RyuJIT and Roslyn?

---

### What is the difference between AppDomain, Assembly, Process, and a Thread?

---

### What is the difference between CIL and MSIL (IL)?

---

### Why does .NET Standard library exist?

---

### Explain how does Asynchronous tasks (Async/Await) work in .NET?

---

### Why does .NET use a JIT compiler instead of just compiling the code once on the target machine?

---

### What are benefits of using JIT?

---

### How to choose the target version of .NET Standard library?

---

### What is the difference between Node.js async model and async/await in .NET?

---

### Explain Finalize vs Dispose usage?

---

### How many types of JIT Compilations do you know?

---

🔹 52. Could you name the difference between .Net Core, Portable, Standard, Compact, UWP, and PCL?
