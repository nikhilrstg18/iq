# .Net Core Interview Questions & Answers 🌹 [![GitHub](https://img.shields.io/github/license/nikhilrstg18/iq?color=blue)](https://github.com/nikhilrstg18/iq/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/nikhilrstg18/iq) ![GitHub forks](https://img.shields.io/github/forks/nikhilrstg18/iq)

> Click :star: if you like the project. Pull Requests are highly appreciated.

> [![Twitter](https://img.shields.io/twitter/follow/rustagi_nikhil?label=Follow%20%40rustagi_nikhil&style=social)](https://twitter.com/rustagi_nikhil) for technical updates.

---

## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---

### Table of Contents

| No. | Questions                                                                                                                                                                                            |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is .Net • .Net Standard • .Net Framework • .Net Core • .Net5? 🚀](#What-is-.Net-•-.Net-Standard-•-.Net-Framework-•-.Net-Core-•-.Net5)                                                          |
| 2   | [What are some characteristics of .NET Core or Why choose .Net Core ?](#What-are-some-characteristics-of-.NET-Core-?-Why-Choose-.Net-Core-?)                                                         |
| 3   | [Explain what is included in .NET Core ?](#explain-what-is-included-in-.NET-Core)                                                                                                                    |
| 4   | [.NET Core Vs Mono ?](#.NET-Core-Vs-Mono-?)                                                                                                                                                          |
| 5   | [What is .NET Framework?](#what-is-.net-framework)                                                                                                                                                   |
| 6   | [What is .NET Standard and why we need to consider it? 🚀](#what-is-.net-standard-and-why-we-need-to-consider-it)                                                                                    |
| 7   | [What is CLR ? 🚀](#what-is-clr)                                                                                                                                                                     |
|     | [Name some Service of CLR.](#Service-of-CLR)                                                                                                                                                         |
|     | [Name some Benefits of CLR.](#Benefits-of-CLR)                                                                                                                                                       |
|     | [What is CoreCLR ?](#What-is-CoreCLR)                                                                                                                                                                |
| 8   | [What is CLS ? 🚀](#what-is-cls)                                                                                                                                                                     |
| 9   | [What is CTS ? 🚀](#what-is-cts)                                                                                                                                                                     |
| 10  | [What is Garbage Collector ? 🚀](#what-is-garbage-collector)                                                                                                                                         |
| 11  | [What is JIT Compiler ? 🚀](#what-is-jit-compiler)                                                                                                                                                   |
| 12  | [What is MSIL ?](#What-is-**MSIL**-or-CIL)                                                                                                                                                           |
| 13  | [What's the difference between SDK and Runtime in .NET Core ?](#What's-the-difference-between-SDK-and-Runtime-in-.NET-Core)                                                                          |
| 14  | [What is the difference between decimal, float and double in .NET 🚀](#What-is-the-difference-between-decimal,-float-and-double-in-.NET)                                                             |
| 15  | [What is difference between .NET Core and .NET Framework and Xamarin ?](#What-is-difference-between-.NET-Core-and-.NET-Framework-and-Xamarin)                                                        |
| 16  | [What about NuGet packages and packages.config ?](#What-about-NuGet-packages-and-packages.config)                                                                                                    |
| 17  | [Talk about new .csproj file ?](#Talk-about-new-.csproj-file)                                                                                                                                        |
| 18  | [Explain the difference between “managed” and “unmanaged” code ? 🚀](#Explain-the-difference-between-“managed”-and-“unmanaged”-code)                                                                 |
| 19  | [Why to use of the IDisposable interface ?](#Why-to-use-of-the-IDisposable-interface)                                                                                                                |
| 20  | [Explain the difference between Task and Thread in .NET ?](#Explain-the-difference-between-Task-and-Thread-in-.NET)                                                                                  |
| 21  | [What is the difference between Class Library (.NET Standard) and Class Library (.NET Core)? 🚀](<#What-is-the-difference-between-Class-Library-(.NET-Standard)-and-Class-Library-(.NET-Core)?>)     |
| 22  | [What's is BCL? What is FCL? 🚀](#What's-is-BCL?-What-is-FCL?)                                                                                                                                       |
| 23  | [Does .NET support multiple inheritance?](#Does-.NET-support-multiple-inheritance?)                                                                                                                  |
| 24  | [What's the difference between RyuJIT and Roslyn? 🚀](#What's-the-difference-between-RyuJIT-and-Roslyn?)                                                                                             |
| 25  | [What is the difference between AppDomain, Assembly, Process, and a Thread? 🚀](#What-is-the-difference-between-AppDomain,-Assembly,-Process,-and-a-Thread?)                                         |
| 26  | [Explain how does Asynchronous tasks (Async/Await) work in .NET? 🚀](<#Explain-how-does-Asynchronous-tasks-(Async/Await)-work-in-.NET?>)                                                             |
| 27  | [Why does .NET use a JIT compiler instead of just compiling the code once on the target machine? ](#Why-does-.NET-use-a-JIT-compiler-instead-of-just-compiling-the-code-once-on-the-target-machine?) |
| 28  | [What is the difference between Node.js async model and async/await in .NET? 🚀](#What-is-the-difference-between-Node.js-async-model-and-async/await-in-.NET?)                                       |
| 29  | [What is the difference between String and string in C#?](#What-is-the-difference-between-String-and-string-in-C#?)                                                                                  |
| 30  | [What is Kestral Server?](#What-is-Kestral-Server?)                                                                                                                                                  |

---

1. ### What is .Net • .Net Standard • .Net Framework • .Net Core • .Net5

   > **.NET**

   - is a `developer platform` made up of `tools`, `programming languages`, and `libraries` for building many different types of applications.

   - There are various implementations of .NET. Each implementation allows .NET code to execute in different places—Linux, macOS, Windows, iOS, Android, and many more

   > **.NET Framework**

   is the `original implementation` of .NET. It supports running websites, services, desktop apps, and more `on Windows`

    <img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/netstandard.png" alt=".Net Standard Vs .Net Core Vs .Net Framework" width=600px />

   > **.NET Standard**

   is a `formal specification of the APIs` that are common across .NET implementations. This allows the same `code` and `libraries` to run on different implementations. (Think of it as an Interface)

   > **Xamarin/Mono**

   is a `.NET` implementation for running `apps on all the major mobile operating systems`, including iOS and Android

   > **.NET Core**

   is a **Open Source**, **Cross-Platform**, **Cloud-optimizaed** implementation of .Net for running `websites, services, and console apps on Windows, Linux, and macOS`. .NET Core is open source on [GitHub](https://github.com/dotnet/core)

   > **.Net5**

   - .NET 5.0 is the next major release of .NET Core following 3.1
   - skipped version numbers 4.x to avoid confusion with .NET Framework 4.x
   - dropped "Core" from the name to emphasize that this is the main implementation of .NET going forward.
     .NET 5.0 supports more types of apps and more platforms than .NET Core or .NET Framework
   - ASP.NET Core 5.0 is based on .NET 5.0 but retains the name "Core" to avoid confusing it with ASP.NET MVC 5. Likewise, Entity Framework Core 5.0 retains the name "Core" to avoid confusing it with Entity Framework 5 and 6

2. ### What are some characteristics of .NET Core ? Why Choose .Net Core ?

   - **Open source**: The .NET Core platform is open source, using MIT and Apache 2 licenses. Documentation is licensed under CC-BY. .NET Core is a .NET Foundation project.

   - **Cross-platform**: Runs on Windows, macOS and Linux; can be ported to other OSes. The supported Operating Systems (OS), CPUs and application scenarios will grow over time, provided by Microsoft, other companies, and individuals.

   - **Command-line tools**: All product scenarios can be exercised at the command-line.

   - **Compatible**: .NET Core is compatible with .NET Framework, Xamarin and Mono, via the .NET Standard Library.

   - **Flexible deployment**: Can be included in your app or installed side-by-side user- or machine-wide.

   - **Supported by Microsoft**: .NET Core is supported by Microsoft, per .NET Core Support

3. ### Explain what is included in .NET Core ?

   .NET Core has 2 major components.

   > CoreCLR (Runtime)

   - is a runtime for .Net Core that is built from the same codebase as the .NET Framework CLR aka **CoreCLR** aka `.NET Core runtime`
   - It includes the same **GC** and **JIT** (RyuJIT), but doesn’t include features like Application Domains or Code Access Security.
   - The runtime is delivered via NuGet, as part of the ASP.NET Core package.

   > BCL (Base Class Libraries) aka Standard Library

   - .NET Core also includes the base class libraries **(BCL)**.
   - These libraries are largely the same code as the .NET Framework class libraries, but have been factored (removal of dependencies) to enable to ship a smaller set of libraries.
   - These libraries are shipped as `System.*` NuGet packages on [nuget.org](https://www.nuget.org/) like
     - `System.Collections`
     - `System.Linq`
     - `System.IO`
     - `System.Data`
     - `System.Reflection`
     - `System.Text`

4. ### .NET Core Vs Mono ?

   - Mono is **third party implementation of .Net Framework for Linux/Android/iOS**

   - .Net Core is **Microsoft's own implementation for cross-platform execution**.

   **[⬆ Back to Top](#table-of-contents)**

---

5. ### What is .NET Framework

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

6. ### What is .NET Standard and why we need to consider it

   **.NET Standard**

   > is a formal specification of .NET APIs (think of it as an Interface) that are intended to be available on all .NET implementations

   or

   > is a set of APIs that all .NET platforms have to implement.

   This unifies the .NET platforms and prevents future fragmentation.

   - **.NET Standard** solves the code sharing problem for .NET developers across all platforms by bringing all the APIs that you expect and love across the environments that you need: desktop applications, mobile apps & games, and cloud services:
   - **.NET Standard** 2.0 will be implemented by .NET Framework, .NET Core, and Xamarin. For .NET Core, this will add many of the existing APIs that have been requested.
   - **.NET Standard** 2.0 includes a compatibility shim for .NET Framework binaries, significantly increasing the set of libraries that you can reference from your **.NET Standard** libraries.
   - **.NET Standard** will replace Portable Class Libraries (PCLs) as the tooling story for building multi-platform .NET libraries

   **[⬆ Back to Top](#table-of-contents)**

---

7. ### What is CLR

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
   - Security also increases as it analyzes the **MSIL** instructions whether they are safe or unsafe. Also, the use of delegates in place of function pointers enhance the type safety and security.
   - Provides cross-language integration because CTS inside CLR provides a common standard that activates the different languages to extend and share each other’s libraries.
   - Provides support to use the components that developed in other .NET programming languages.
   - It allows easy creation of scalable and multithreaded applications, as the developer has no need to think about the memory management and security issues.

   > #### What is CoreCLR

   - CoreCLR is the execution engine in .NET Core, performing functions such as garbage collection and compilation to machine code

   **[⬆ Back to Top](#table-of-contents)**

---

8. ### What is CLS

   - CLS is subset of CTS and deals in **Language Interoperability**
   - Responsible for converting the different .NET programming language syntactical rules and regulations into CLR understandable format (i.e. **MSIL**).
   - Basically, it provides the Language Interoperability (i.e. to provide the execution support to other programming languages also in .NET framework).

   `Language Interoperability` can be achieved in two ways :

   > **Managed Code**:

   - The `**MSIL**` code which is managed by the `CLR` is known as the `Managed Code`. For managed code CLR provides three .NET facilities:
     - **CAS** (Code Access Security)
     - Exception Handling
     - Automatic Memory Management.

   > **Unmanaged Code**:

   - Before .NET development the programming language like .COM Components & Win32 API do not generate the **MSIL** code. So these are not managed by `CLR` rather managed by Operating System.
   - Anything you've used to Invoke calls to get outside of the nice comfy world of everything available to you in the .NET Framwork is unmanaged – and you're now responsible for cleaning it up.

   **[⬆ Back to Top](#table-of-contents)**

---

9. ### What is CTS

   - CTS is superset of CLS and deals with data type.
   - Every programming language has its own data type system, so CTS is responsible for understanding all the data type systems of .NET programming languages and converting them into CLR understandable format which will be a common format (i.e. **MSIL**).

   There are 2 Types of CTS that every .NET programming language have :

   > **Value Types**:

   - Value Types will `store the value directly into the memory location`.
   - These types work with **Stack mechanism**, i.e. CLR allows memory for these at Compile Time.

   > **Reference Types**:

   - Reference Types will `contain a memory address of value because the reference types won’t store the value directly in memory`. \
   - These types work with **Heap mechanism**, i.e. CLR allots memory at Runtime.

   **[⬆ Back to Top](#table-of-contents)**

---

10. ### What is Garbage Collector

    - A Garbage Collector is an automatic memory manager.
    - Garbage collection is a process of releasing the memory used by the objects that are no longer referenced.
    - It has the following advantages

      - it allows us to develop an application without having to free memory
      - it efficiently allocates an object on the managed heap and reclaims object memories that are no longer being used.
      - Provides memory safety by making sure that an object cannot use the content of another object

    - The CLR initializes the garbage collector, then the CLR allocates a segment of memory to store and manage object(s). This is called the **managed heap**. \
      The managed heap is for each managed process, in other words all threads in the process allocate memory for objects in the same heap memory.

      > #### Heap Generation
      >
      > \
      >  The heap is organized into generations so it can handle long-lived and short-lived objects.

      There are three generations of objects on the heap:

        <img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/gc-heap-gen.png" alt="Illustration GC heap Generations" width=400px height=350px/>

      **Generation 0**:

      - This is the youngest generation and contains short-lived objects. An example of a short-lived object is a temporary variable. Garbage collection occurs most frequently in this generation.
      - Newly allocated objects form a new generation of objects and are implicitly Gen 0 collections unless they are large objects, in which case they go on the large object heap in a Gen 2 collection.
      - Most objects are reclaimed for garbage collection in Gen 0 and do not survive to the next generation. Objects that survive a Gen 0 garbage collection are promoted to Gen 1.

      **Generation 1**:

      - This generation contains short-lived objects and acts as a buffer between short-lived objects and long-lived objects. Objects that survive a Gen 1 garbage collection are promoted to Gen 2.

      **Generation 2**:

      - This generation contains long-lived objects. An example of a long-lived object is an object in a server application that contains static data that lives for the duration of the process. Objects that survive a Gen 2 garbage collection remain in Gen 2.
      - Collecting a generation means collecting objects in that generation and all its younger generations. A Gen 2 garbage collection is also known as a full garbage collection because it reclaims all objects in all generations. \

      > #### How Garbage Collector Works
      >
      > \
      >  A garbage collection has the following phases:

      - **Marking** : Finds and creates a list of all live objects.
      - **Relocating** : Updates the references to the objects that will be compacted.
      - **Compacting** : Reclaims the space occupied by the dead objects and compacts the surviving objects. The compacting phase moves objects that have survived a garbage collection toward the older end of the segment. (Ordinarily, the large object heap is not compacted, because copying large objects imposes a performance penalty.)

      The GC uses the following information to determine whether objects are live:

    <img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/gc-wokring.png" alt="Illustration How GC works" width=450px height=300px/>

    - **Stack roots**: Stack variables provided by the just-in-time (JIT) compiler and stack walker.
    - **Garbage collection handles**: Handles that point to managed objects and that can be allocated by user code or by the CLR.
    - **Static data**: Static objects in application domains that could be referencing other objects.

    In addition, there are unmanaged resources like file streams, network/database connections that you need to take special care of. You need to use **Finalizer** & **Dispose** in this case

    #### Explain Finalize vs Dispose usage?

    | Basis For comparison | Dispose()                                      | Finalize()                                             |
    | -------------------- | ---------------------------------------------- | ------------------------------------------------------ |
    | Defined              | in the interface **IDisposable**               | in **Object** class                                    |
    | Invoked by           | user                                           | Garbage Collector                                      |
    | Implementation       | when there is a close()                        | unmanaged resources                                    |
    | Purpose              | free unmanaged resource whenever it is inovked | free unmanaged resource before the object is destroyed |
    | Access declared      | public                                         | private                                                |
    | Action               | faster and instantly disploses an object       | slower                                                 |

    **[⬆ Back to Top](#table-of-contents)**

---

11. ### What is JIT Compiler

    JIT stands for **Just In Time**. \
     It is responsible for converting the **MSIL** or **CIL** (Common Intermediate Language) into machine code or native code using the **CLR** environment. \
     Before a computer can execute the source code, special programs called compilers must rewrite it into machine instructions, also known as object code. This process (commonly referred to simply as “compilation”) can be done explicitly or implicitly.

    Implicit compilation is a two-step process:

    - The first step is converting the source code to Intermediate Language (**IL**) by a language-specific compiler.
    - The second step is converting the IL to machine instructions.

    The main difference with the explicit compilers is that only executed fragments of IL code are compiled into machine instructions, at runtime. The .NET framework calls this compiler the JIT (Just-In-Time) compiler.

    3 JIT compiler types as below:

    - **Pre-JIT Compiler** (Compiles entire code into native code completely)
    - **Econo JIT Compiler** (Compiles code part by part freeing when required)
    - **Normal JIT Compiler** (Compiles only that part of code when called and places in cache

    **[⬆ Back to Top](#table-of-contents)**

---

12. ### What is **MSIL** or CIL

    - When we compile our .NET code then it is not directly converted to native/binary code; it is first converted into intermediate code known as **MSIL** code which is then interpreted by the CLR.
    - **MSIL** is independent of hardware and the operating system. Cross language relationships are possible since **MSIL** is the same for all .NET languages. **MSIL** is further converted into native code.

    **[⬆ Back to Top](#table-of-contents)**

---

13. ### What's the difference between SDK and Runtime in .NET Core

    > The **SDK** is all of the stuff that is needed/makes developing a .NET Core application easier, such as the CLI and a compiler.

    > The **runtime** is the "virtual machine" that hosts/runs the application and abstracts all the interaction with the base operating system.

**[⬆ Back to Top](#table-of-contents)**

---

14. ### What is the difference between decimal, float and double in .NET

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

15. ### What is difference between .NET Core and .NET Framework and Xamarin

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

16. ### What about NuGet packages and packages.config

    There is no more packages.config file. All packages are now managed within .csproj file.

    The .csproj file has been cleaned up and it also serves the role of packages.config(or package.json for Node devs). That means that’s where your packages and versions will be saved.

    NuGet packages are the unit of reference and they can depend on other NuGet packages, but also they can depend on projects. And as before, projects can also depend on NuGet packages and other projects. That means that projects and NuGet packages are interchangeable.

    With .NET Core, you can easily turn your projects into NuGet packages, with one click inside of the properties.

**[⬆ Back to Top](#table-of-contents)**

---

17. ### Talk about new .csproj file

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

18. ### Explain the difference between “managed” and “unmanaged” code

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

19. ### Why to use of the IDisposable interface

    The "primary" use of the IDisposable interface is to clean up unmanaged resources.

    Note the purpose of the Dispose pattern is to provide a mechanism to clean up both managed and unmanaged resources and when that occurs depends on how the Dispose method is being called.

**[⬆ Back to Top](#table-of-contents)**

---

20. ### Explain the difference between Task and Thread in .NET

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

21. ### What is the difference between Class Library (.NET Standard) and Class Library (.NET Core)?

- **Compatibility**: Libraries that target .NET Standard will run on any .NET Standard compliant runtime, such as .NET Core, .NET Framework, Mono/Xamarin. On the other hand, libraries that target .NET Core can only run on the .NET Core runtime.
- **API Surface Area**: .NET Standard libraries come with everything in **NETStandard.Library**, whereas .NET Core libraries come with everything in **Microsoft.NETCore.App** (includes approx. 20 additional libraries )

> Why do they both exists ?

- Ignoring libraries for a moment, the reason that **.NET Standard exists is for portability**; it defines a set of APIs that .NET platforms agree to implement.
- Any platform that implements a .NET Standard is compatible with libraries that target that .NET Standard. One of those compatible platforms is .NET Core.

**[⬆ Back to Top](#table-of-contents)**

---

22. ### What's is BCL? What is FCL?

<img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/bcl.png" alt="Illustration How GC works" width=400px height=450px/>

> BCL

- BCL is subset of FCL
- **A .NET Framework library**, BCL is the standard for the C# runtime library and one of the Common Language Infrastructure (CLI) standard libraries. BCL provides types representing the built-in CLI data types, basic file access, collections, custom attributes, formatting, security attributes, I/O streams, string manipulation, and more.
  for eg. **System**, **System.Data**, **System.Web**, etc

> FCL

- FCL is superset of BCL
- **The .NET Framework class library** is exactly what its name suggests: a library of classes and other types that developers can use to make their lives easier. While these classes are themselves written in C#, they can be used from any CLR based language
- For eg. **Microsoft.AspNetCore**, **Microsoft.EntityFrameworkCore**, etc.

**[⬆ Back to Top](#table-of-contents)**

---

23. ### Does .NET support multiple inheritance?

No

**[⬆ Back to Top](#table-of-contents)**

---

24. ### What's the difference between RyuJIT and Roslyn?

- **Roslyn** : Cross-platform Compiler that compiles source code (C#, F#, etc) to IL code
- **RyuJIT** : JIT compiler that compiles your IL code to native Code

**[⬆ Back to Top](#table-of-contents)**

---

25. ### What is the difference between AppDomain, Assembly, Process, and a Thread?

- An **AppDomain** is an isolation unit within a process. AppDomains can be created at runtime, loaded with code, and unloaded. Its an isolation boundary designed to make .NET apps more reliable.

- An **assembly** holds one or more modules, which hold compiled chunks of code. You will typically see an assembly as an .EXE or a .DLL.

- A **process** is an executing application (waaaay oversimplified).

- A **thread** is an execution context. The operating system executes code within a thread. The operating system switches between threads, allowing each to execute in turn, thus giving the impression that multiple applications are running at the same time.

To put it all together (very simplified)...

A program is executed. A process is created by the operating system, and within its single thread it starts loading code to execute. In a .NET application, a single AppDomain is created by the CLR. The application's executing assembly (the .EXE) is loaded into this AppDomain and begins execution. The application can spawn new processes, create AppDomains, load other assemblies into these domains, and then create new Threads to execute code in any of these AppDomains.

**[⬆ Back to Top](#table-of-contents)**

---

26. ### Explain how does Asynchronous tasks (Async/Await) work in .NET?

    👉 [async/await with code example](https://www.c-sharpcorner.com/article/async-and-await-in-c-sharp/)

**[⬆ Back to Top](#table-of-contents)**

---

27. ### Why does .NET use a JIT compiler instead of just compiling the code once on the target machine?

- If a code executing on a target machine calls a non-native method, the JIT compiler converts the MSIL of that method into native code.
- The JIT compiler also enforces type-safety in the runtime environment of the .NET Framework.
- It checks for the values that are passed to parameters of any method.

**[⬆ Back to Top](#table-of-contents)**

---

28. ### What is the difference between Node.js async model and async/await in .NET?

- One difference is that Node.js is asynchronously single-threaded, while ASP.NET is asynchronously multi-threaded. This means the Node.js code can make some simplifying assumptions, because all your code always runs on the same exact thread
- So when your ASP.NET code awaits, it could possibly resume on a different thread

**[⬆ Back to Top](#table-of-contents)**

---

29. ### What is the difference between String and string in C#?

    `string` is an alias in C# for `System.String`. So technically, there is no difference. It's like `int` vs. `System.Int32`.

    As far as guidelines, it's generally recommended to use `string` any time you're referring to an object.

    ```csharp
    string place = "world";
    ```

    Likewise, it's generally recommended to use `String` if you need to refer specifically to the class.

    ```csharp
    string greet = String.Format("Hello {0}!", place);
    ```

**[⬆ Back to Top](#table-of-contents)**

---

30. ### What is Kestral Server?

    Kestrel is an edge server that is cross-platform used for serving web applications that run on .NET core

**[⬆ Back to Top](#table-of-contents)**

---
