# .Net Core Interview Questions & Answers 🌹 [![GitHub](https://img.shields.io/github/license/nikhilrstg18/iq?color=blue)](https://github.com/nikhilrstg18/iq/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/nikhilrstg18/iq) ![GitHub forks](https://img.shields.io/github/forks/nikhilrstg18/iq)

> Click :star: if you like the project. Pull Requests are highly appreciated.

> [![Twitter](https://img.shields.io/twitter/follow/rustagi_nikhil?label=Follow%20%40rustagi_nikhil&style=social)](https://twitter.com/rustagi_nikhil) for technical updates.

---

## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---

### Table of Contents

| No. | Questions                                                 |
| --- | --------------------------------------------------------- |
| 1   | [What is .NET core ?](#what-is-.net-core)                 |
| 2   | [What is CLR ?](#what-is-clr)                             |
| 3   | [What is CLS ?](#what-is-cls)                             |
| 4   | [What is CTS ?](#what-is-cts)                             |
| 5   | [What is Garbage Collector ?](#what-is-garbage-collector) |
| 6   | [What is JIT Compiler ?](#what-is-jit-compiler)           |
| 7   | [What is MSIL ?](#what-is-msil)                           |

---

1. ### What is .Net Core

   The [.NET Core](https://dotnet.microsoft.com/download) platform is a new .NET stack that is optimized for open source development and agile delivery on NuGet.

   .NET Core has two major components. It includes a small runtime that is built from the same codebase as the .NET Framework CLR. The .NET Core runtime includes the same **GC** and **JIT** (RyuJIT), but doesn’t include features like Application Domains or Code Access Security. The runtime is delivered via NuGet, as part of the ASP.NET Core package.

   .NET Core also includes the base class libraries **(BCL)**. These libraries are largely the same code as the .NET Framework class libraries, but have been factored (removal of dependencies) to enable to ship a smaller set of libraries. These libraries are shipped as `System.*` NuGet packages on [nuget.org](https://www.nuget.org/)

   **[⬆ Back to Top](#table-of-contents)**

---

2. ### What is CLR

   The CLR stands for `Common Language Runtime` and it is an Runtime Environment in .Net.

   <img align="right" src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/clr.png" alt="Illustration level at which CLR operates" width=400px height=350px/>

   Main components of CLR:

   - **Common Language Specification** (**CLS**)
   - **Common Type System** (**CTS**)
   - **Garbage Collection** (**GC**)
   - **Just In – Time** Compiler (**JIT**)

   It works as a layer between Operating Systems and the applications written in .NET languages that conforms to the Common Language Specification (CLS).

   The main function of Common Language Runtime (CLR) is to convert the Managed Code into native code and then execute the program.

   > Benefits of CLR:

   - It improves the performance by providing a rich interact between programs at run time.
   - Support automatic memory management with the help of Garbage Collector.
   - Enhance portability by removing the need of recompiling a program on any operating system that supports it.
   - Provide language, platform, and architecture independence.
   - Security also increases as it analyzes the MSIL instructions whether they are safe or unsafe. Also, the use of delegates in place of function pointers enhance the type safety and security.
   - Provides cross-language integration because CTS inside CLR provides a common standard that activates the different languages to extend and share each other’s libraries.
   - Provides support to use the components that developed in other .NET programming languages.
   - It allows easy creation of scalable and multithreaded applications, as the developer has no need to think about the memory management and security issues.

   **[⬆ Back to Top](#table-of-contents)**

---

3. ### What is CLS

   It is responsible for converting the different .NET programming language syntactical rules and regulations into CLR understandable format. Basically, it provides the Language Interoperability. Language Interoperability means to provide the execution support to other programming languages also in .NET framework.

   `Language Interoperability` can be achieved in two ways :

   > **Managed Code**:\
   >  The `MSIL` code which is managed by the `CLR` is known as the `Managed Code`.
   > For managed code CLR provides three .NET facilities:

   - **CAS** (Code Access Security)
   - Exception Handling
   - Automatic Memory Management.\

   > **Unmanaged Code**: \
   >  Before .NET development the programming language like .COM Components & Win32 API do not generate the MSIL code. So these are not managed by `CLR` rather managed by Operating System.

   **[⬆ Back to Top](#table-of-contents)**

---

4. ### What is CTS

   Every programming language has its own data type system, so CTS is responsible for understanding all the data type systems of .NET programming languages and converting them into CLR understandable format which will be a common format.

   There are 2 Types of CTS that every .NET programming language have :

   > **Value Types**: \
   >  Value Types will `store the value directly into the memory location`. \
   >  These types work with stack mechanism only.  
   >  CLR allows memory for these at Compile Time.\
   > **Reference Types**: \
   >  Reference Types will `contain a memory address of value because the reference types won’t store the variable value directly in memory`. \
   >  These types work with Heap mechanism.
   > CLR allots memory for these at Runtime.

   **[⬆ Back to Top](#table-of-contents)**

---

5. ### What is Garbage Collector

   It is used to provide the Automatic Memory Management feature. \
    If there was no garbage collector, programmers would have to write the memory management codes which will be a kind of overhead on programmers.

   **[⬆ Back to Top](#table-of-contents)**

---

6. ### What is JIT Compiler

   JIT stands for **Just In Time**. \
    It is responsible for converting the `MSIL` or `CIL`(Common Intermediate Language) into machine code or native code using the `Common Language Runtime` environment.

   **[⬆ Back to Top](#table-of-contents)**

---

7. ### What is MSIL or CIL

   When we compile our .NET code then it is not directly converted to native/binary code; it is first converted into intermediate code known as MSIL code which is then interpreted by the CLR. MSIL is independent of hardware and the operating system. Cross language relationships are possible since MSIL is the same for all .NET languages. MSIL is further converted into native code.

   **[⬆ Back to Top](#table-of-contents)**

---
