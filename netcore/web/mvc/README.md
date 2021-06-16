# Asp.Net MVC Core Interview Questions & Answers 🌹 [![GitHub](https://img.shields.io/github/license/nikhilrstg18/iq?color=blue)](https://github.com/nikhilrstg18/iq/blob/master/LICENSE.md) ![GitHub stars](https://img.shields.io/github/stars/nikhilrstg18/iq) ![GitHub forks](https://img.shields.io/github/forks/nikhilrstg18/iq)

> Click :star: if you like the project. Pull Requests are highly appreciated.

> [![Twitter](https://img.shields.io/twitter/follow/rustagi_nikhil?label=Follow%20%40rustagi_nikhil&style=social)](https://twitter.com/rustagi_nikhil) for technical updates.

---

## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---

### Table of Contents

| No. | Questions                                                                                                                                              |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | [What is MVC? 🚀](#What-is-MVC?)                                                                                                                       |
| 2   | [Breifly explain project structure of Asp.Net Core Application (Empty)? 🚀](<#Breifly-explain-project-structure-of-Asp.Net-Core-Application-(Empty)?>) |

---

1. ### What is MVC?

   > **M** --> Model \
   > **V** --> View \
   > **C** --> Controller

---

2. ### Breifly explain project structure of Asp.Net Core Application (Empty)?

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

   - Here `Program` class has static method called `Main()` i.e. **entry point of Asp.Net Core application**. In Fact, Asp.Net Core Apps are nothing but Console Apps

   - `Main()` invokes another static method called **CreateHostBuilder(args)** which returns **IHostBuilder** instance \
     and invokes **.Build()** to run the given actions to initialize the web host on `HostBuilder` instance from `CreateHostBuilder(args)` \
     and finally **.Run()** to run an application and block the calling thread untill host is shutdown on `IHostBuilder` instance from `.Build()`

   - Here in **`CreateHostBuilder(args)`** \
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

   - Then **ConfigureWebHostsDefaults( webBuilder => { webBuilder.UseStartup<Startup>();})** Configures a `Microsoft.Extensions.Hosting.IHostBuilder` with defaults for hosting a web app. defaults are defined in **Startup** \
     The following defaults are applied to the Microsoft.Extensions.Hosting.IHostBuilder:

     - use **Kestrel** as the web server and configure it using the application's configuration providers

     - configure `Microsoft.AspNetCore.Hosting.IWebHostEnvironment.`**WebRootFileProvider** to **include static web assets** from projects referenced by the entry assembly during development

     - adds the **HostFiltering middleware**

     - adds the **ForwardedHeaders middleware** if ASPNETCORE_FORWARDEDHEADERS_ENABLED=true,

     - enable **IIS integration**

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
         // This method gets called by the runtime. Use this method to add services to the container.
         public void ConfigureServices(IServiceCollection services)
         {
         }

         // This method gets called by the runtime. Use this method to configure the HTTP request pipeline.
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

   - In the `ConfigureServices()`, we get **IServiceCollection** instance, i.e. the entry point to add items to our service collection, so that we can leverage depedency injection container that comes with Asp.Net Core out of the box.

   - In the `Configure()`, we define our http request pipeline configuration
     notice .**UseDeveloperExceptionPage()**, **UseRouting()** and **UseEndpoints()** are middleware their order in which are declared is significant

---

more comming soon...
