# Asp.Net Core MVC Interview Questions & Answers 🌹 [![GitHub](https://img.shields.io/github/license/nikhilrstg18/iq?color=blue)](https://github.com/nikhilrstg18/iq/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/nikhilrstg18/iq) ![GitHub forks](https://img.shields.io/github/forks/nikhilrstg18/iq)

> Click :star: if you like the project. Pull Requests are highly appreciated.

> [![Twitter](https://img.shields.io/twitter/follow/rustagi_nikhil?label=Follow%20%40rustagi_nikhil&style=social)](https://twitter.com/rustagi_nikhil) for technical updates.

---

## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---

### Table of Contents

| No. | Questions                                                                                                                          |
| --- | ---------------------------------------------------------------------------------------------------------------------------------- |
| 1   | [What is MVC? 🚀](#What-is-MVC?)                                                                                                   |
| 2   | [Explain project structure of Asp.Net Core Application (Empty) 🚀](#Explain-project-structure-of-Asp.Net-Core-Application-Empty)   |
| 3   | [What is Dependency Injection? 🚀](#What-is-Dependency-Injection?)                                                                 |
| 4   | [Briefly explain ConfigureServices() in Startup class 🚀](<#Briefly-explain-ConfigureServices()-in-Startup-class>)                 |
| 5   | [Briefly explain Configure() in Startup class 🚀](<#Briefly-explain-Configure()-in-Startup-class>)                                 |
| 6   | [Briefly explain CreateDefaultBuilder() in Startup class 🚀](<#Briefly-explain-CreateDefaultBuilder()-in-Startup-class>)           |
| 7   | [Briefly explain ConfigureWebHostsDefaults() in Startup class 🚀](<#Briefly-explain-ConfigureWebHostsDefaults()-in-Startup-class>) |

---

1. ### What is MVC?

   > **M** --> Model \
   > **V** --> View \
   > **C** --> Controller

   **[⬆ Back to Top](#table-of-contents)**

---

2. ### Explain project structure of Asp.Net Core Application (Empty)

   <img src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/aspnetcore-empty.png" alt="Empty Asp.Net Core app .csproj" width=300px />

   - **.csproj file** (.Net 3+ version)

   ```xml
   <Project Sdk="Microsoft.NET.Sdk.Web">

   <PropertyGroup>
      <TargetFramework>net5.0</TargetFramework>
   </PropertyGroup>

   </Project>
   ```

   Here net5.0 is called as moniker, signifying the target framework

   - **dependencies**

   <img src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/aspnetcore-deps.png" alt="Asp.Net Core app dependencies" width=300px />

   - **Properties** > **launchSetting.json**

   <img src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/aspnetcore-prop.png" alt="Asp.Net Core app Properties" width=300px />

   ```json
   {
     "iisSettings": {
       "windowsAuthentication": false,
       "anonymousAuthentication": true,
       "iisExpress": {
         "applicationUrl": "http://localhost:49846",
         "sslPort": 44309
       }
     },
     "profiles": {
       "IIS Express": {
         "commandName": "IISExpress",
         "launchBrowser": true,
         "environmentVariables": {
           "ASPNETCORE_ENVIRONMENT": "Development"
         }
       },
       "demo": {
         "commandName": "Project",
         "dotnetRunMessages": "true",
         "launchBrowser": true,
         "applicationUrl": "https://localhost:5001;http://localhost:5000",
         "environmentVariables": {
           "ASPNETCORE_ENVIRONMENT": "Development"
         }
       }
     }
   }
   ```

   - **appsettings.json**

   ```json
   {
     "Logging": {
       "LogLevel": {
         "Default": "Information",
         "Microsoft": "Warning",
         "Microsoft.Hosting.Lifetime": "Information"
       }
     },
     "AllowedHosts": "*"
   }
   ```

   > appsettings.Development.json

   ```json
   {
     "Logging": {
       "LogLevel": {
         "Default": "Information",
         "Microsoft": "Warning",
         "Microsoft.Hosting.Lifetime": "Information"
       }
     }
   }
   ```

   - **Program.cs**

   ```csharp
   using Microsoft.AspNetCore.Hosting;
   using Microsoft.Extensions.Hosting;

   namespace demo
   {
      public class Program
      {
         public static void Main(string[] args)
         {
               CreateHostBuilder(args).Build().Run();
         }

         public static IHostBuilder CreateHostBuilder(string[] args) =>
               Host.CreateDefaultBuilder(args)
                  .ConfigureWebHostDefaults(webBuilder =>
                  {
                     webBuilder.UseStartup<Startup>();
                  });
      }
   }

   ```

   - Here `Program` class has static method called **Main()** i.e. **entry point of Asp.Net Core application**. In Fact, Asp.Net Core Apps are nothing but Console App.

   - `Main()` invokes another static method called **CreateHostBuilder(args)** which returns **IHostBuilder** instance \
     and invokes **.Build()** to run the given actions to initialize the web host on `HostBuilder` instance from `CreateHostBuilder(args)` \
     and finally **.Run()** to run an application and block the calling thread untill host is shutdown on `IHostBuilder` instance from `.Build()`

   - Here in **`CreateHostBuilder(args)`**

     👉 [Understanding CreateDefaultBuilder() ](<#Briefly-explain-CreateDefaultBuilder()-in-Startup-class?>)

     👉 [Understanding ConfigureWebHostsDefaults() ](<#Briefly-explain-ConfigureWebHostsDefaults()-in-Startup-class?>)

   - **Startup.cs**

   ```csharp
   using Microsoft.AspNetCore.Builder;
   using Microsoft.AspNetCore.Hosting;
   using Microsoft.AspNetCore.Http;
   using Microsoft.Extensions.DependencyInjection;
   using Microsoft.Extensions.Hosting;

   namespace demo
   {
      public class Startup
      {
         // This method gets called by the runtime.
         // Use this method to add services to the container.
         public void ConfigureServices(IServiceCollection services)
         {
         }

         // This method gets called by the runtime.
         // Use this method to configure the HTTP request pipeline.
         public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
         {
               if (env.IsDevelopment())
               {
                  // AspNetCore_Environment = Development in launchSetting.json
                  app.UseDeveloperExceptionPage(); // for details exception
               }

               app.UseRouting();

               app.UseEndpoints(endpoints =>
               {
                  endpoints.MapGet("/", async context =>
                  {
                     await context.Response.WriteAsync("Hello World!");
                  });
               });
         }
      }
   }

   ```

   - In the **Startup** class, there are 2 methods **ConfigureServices()** and **Configure()**. These 2 methods are invoked automatically by Asp.Net Core and **they are called by name as you see there are no overrides**.

     👉 [Understanding ConfigureServices()](<#Briefly-explain-ConfigureServices()-in-Startup-class?>)

     👉 [Understanding Configure()](<#Briefly-explain-Configure()-in-Startup-class?>)

   Thus, in the **Startup of Application**

   - Application starting
     - Program Class
       - Startup Class
         - ConfigureServices() // register services
         - Configure() // HTTP pipeline is created
           - Ready for Requests ✔

   **[⬆ Back to Top](#table-of-contents)**

---

3. ### What is Dependency Injection?

   > Understaning Tight Coupling and how DI helps to achieve Loose Coupling.

   ```csharp
   public class My{
      private readonly Logger _logger;

      public My(){
         _loggger = new Logger();
      }
   }

   public class Logger{

      public void Log(){
         //
      }
   }
   ```

   Image, there is **My** class and it needs **Logger** class to log actions. \
   Typically we create the reference of **Logger** class in **My** class by calling new Logger(). \
   Now there is nothing wrong in doing that, we have a **hard dependency** between **My** class and **Logger** class - aka **Tight Coupling**

   ```csharp
   public class My{

      private readonly ILogger _logger;

      public My(){
         _loggger = new Logger();
      }
   }

   public interface ILogger{
      void Log();
   }

   public class Logger:ILogger{

      public void Log(){
         //
      }
   }
   ```

   Minor improvement to solve this issue would to introduce an **Interface**, so MyClass can now work with **ILogger**. But as long as we have to instantiate the **Ilogger** = **new Logger**, we have **tight coupling** between the 2 classes.

   What we need is a way to push a **Logger** instance into **My** class throught constructor parameter \
   With this we basically moved the responsibility of creating an instance up the tree and here comes the **Dependency Injection Container**, iInstead of us manually in the object treee creating all the instances ourselves, we'll have a container do this for us.

   **DI Container** has 2 purposes:

   1. Register the depedencies in the collection of things it knows, the **ILogger** and the **Logger** such that if someone ask for **ILogger**, give them **Logger** instance which is created by the DI Container. This is recursive in resolving dependencies.
   2. Everyone within the application, including My class knows about the **DI Container** and can simply ask it for an instance of **ILogger**, the DI container will then return a fully resolved instance of **Logger** to the callers of **My** class.

   The main goal is to have a centeral place to store all dependencies and being the centeral point to resolve instances for other components

   **[⬆ Back to Top](#table-of-contents)**

---

4. ### Briefly explain ConfigureServices() in Startup class

- In the **ConfigureServices()**, we get **IServiceCollection** instance, i.e. the entry point to add items to our service collection, such that we register services here by leveraging built-in Depedency Injection Container that comes with Asp.Net Core out of the box.

  - Through [**Dependency Injection** 👈](#What-is-Dependency-Injection?), we can achieve much more `loosly coupled architecture within our application`
  - This **DI Container** is available to the **IServiceProvider** interface and the **IServiceCollection** instance is the collection of services it manages.
  - Services are nothing but object with certain functionality for other parts of the application and there can be system services as well as our own services.
  - ASP.Net Core already comes with large number of services,Eg

  ```csharp
  public void ConfigureServices(IServiceCollection services)
  {
     // register framework services
     services.AddControllersWithView(); // to regsiter services for MVC

     // register our own services
  }
  ```

  **[⬆ Back to Top](#table-of-contents)**

---

5. ### Briefly explain Configure() in Startup class

   In the **Configure()**, **HTTP Request Pipeline** will setup
   notice .**UseDeveloperExceptionPage()**, **UseRouting()** and **UseEndpoints()** are middleware their order in which are declared is significant

   - The Request pipeline consist of number of components that are chained behind on another aka **MiddleWare** aka **IHttpModule**
   - **Middlewares** will intercept of handle incoming **Http Request** and produce **Http Response**. Each middleware will be able to alter the request or response, or simply pass it on the next middleware in the pipeline.

      <img src="https://github.com/nikhilrstg18/iq/blob/main/netcore/assets/img/mw-pipeline.png" alt="Middleware pipeline" width=600px />

   - This is how you should image the middleware request pipeline \
     It is compsed of number of MW components sequencially placed behind one another. When a request is sent. \
     When a Http Request is sent to our app, it travels through these MW components. After being handled, the Http Response travels back through same MW components.

   ```csharp
   public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
   {
         app.UseDeveloperExceptionPage();
         app.useStatusCodePages();
         app.useStaticFiles();
         app.UseRouting();
         app.UseEndpoints(endpoints =>
         {
            //...
         });
   }
   ```

   - Here you can see the **Configure()**, where we are registering 5 MW. Each MW will perform some functionality on incoming request or outgoing response
   - One important point to remember about MW components is that since these are added behind one another, **order in which they are added is signifincant**
   - Typically, you call to add the endpoint MW needs to be at the end of pipeline. MW to compress the response should be added after response of endpoint and Static Files MW, otherwise static files would never get compressed.```

   **[⬆ Back to Top](#table-of-contents)**

---

6. ### Briefly explain CreateDefaultBuilder() in Startup class

   ```csharp
   public static IHostBuilder CreateHostBuilder(string[] args) =>
      Host.CreateDefaultBuilder(args)
         .ConfigureWebHostDefaults(webBuilder =>
         {
            webBuilder.UseStartup<Startup>();
         });
   ```

   **Host.CreateDefaultBuilder(args)** : Initializes a new instance of the `Microsoft.Extensions.Hosting.HostBuilder` class with pre-configured defaults \
   The following defaults are applied to the returned Microsoft.Extensions.Hosting.HostBuilder:

   - set the `Microsoft.Extensions.Hosting.IHostEnvironment.`**ContentRootPath** to the result of `System.IO.Directory.`**GetCurrentDirectory**

   - load host `Microsoft.Extensions.Configuration.IConfiguration` from "**DOTNET\_**" environment variables

   - load host `Microsoft.Extensions.Configuration.IConfiguration`\* from supplied **command line args**

   - load app `Microsoft.Extensions.Configuration.IConfiguration` from **'appsettings.json'**
     and **'appsettings.[Microsoft.Extensions.Hosting.IHostEnvironment.EnvironmentName].json'**

   - load app `Microsoft.Extensions.Configuration.IConfiguration` from **User Secrets** when `Microsoft.Extensions.Hosting. HostEnvironment.EnvironmentName` is **'Development'** using the entry assembly

   - load app `Microsoft.Extensions.Configuration.IConfiguration` from **environment variables**

   - load app `Microsoft.Extensions.Configuration.IConfiguration` from supplied **command line args**

   - configure the `Microsoft.Extensions.Logging.ILoggerFactory` to **log to the console**, debug, and event source output

   - enables scope validation on the dependency injection container when `Microsoft.Extensions.Hosting.IHostEnvironment.EnvironmentName` is **Development**

   **[⬆ Back to Top](#table-of-contents)**

---

7. ### Briefly explain ConfigureWebHostsDefaults() in Startup class

   ```csharp
   public static IHostBuilder CreateHostBuilder(string[] args) =>
      Host.CreateDefaultBuilder(args)
         .ConfigureWebHostDefaults(webBuilder =>
         {
            webBuilder.UseStartup<Startup>();
         });
   ```

   **ConfigureWebHostsDefaults( webBuilder => { webBuilder.UseStartup<Startup>();})** Configures a `Microsoft.Extensions.Hosting.IHostBuilder` with defaults for hosting a web app. defaults are defined in **Startup**

   The following defaults are applied to the Microsoft.Extensions.Hosting.IHostBuilder:

   - use **Kestrel** as the web server and configure it using the application's configuration providers

   - configure `Microsoft.AspNetCore.Hosting.IWebHostEnvironment.`**WebRootFileProvider** to **include static web assets** from projects referenced by the entry assembly during development

   - adds the **HostFiltering middleware**

   - adds the **ForwardedHeaders middleware** if ASPNETCORE_FORWARDEDHEADERS_ENABLED=true,

   - enable **IIS integration**

   **[⬆ Back to Top](#table-of-contents)**

---

more comming soon...
