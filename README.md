# Tech Notes on 2025
+ [HTML5](https://github.com/gtechsltn/HTML5-API-Paste-Image-From-Clipboard)
+ [GitHub Actions](https://github.com/gtechsltn/AspNetCoreAPI-GitHubAction)
+ [Security (Authentication + Authorization) in ASP.NET Core](https://docs.google.com/document/d/1sN38JmL0MWNPHAhd2KcHuKXqpxxrudWzvNYMmXSeWAw)
+ [Serilog in Console App](https://github.com/gtechsltn/Console-App-Code-Generator)
+ [Serilog in ASP.NET Core](https://github.com/gtechsltn/LoggingWithSerilog/tree/master/Src/LoggingWithSerilog/ASPNETCoreMVCWebApp)
  + .NET Core 10
  + ASP.NET Core MVC Web Application
  + ASP.NET Core Web API
  + SQL Server (Users, Roles, UserRoles)
  + Serilog
  + ADO.NET
  + EF Core
  + Role-Based Access Control (RBAC) with JWT Access Token, Refresh Token, Revoke Token
  + [Seed Data](https://github.com/gtechsltn/EFCoreSeedDataGenerator)
  + Stored Procedures
+ [Unicode in Serilog + Log4Net](https://docs.google.com/document/d/1YrCm7KrDgzES0t4W8XPn587-xwAEYXqQtSwyRSJhS4w)
+ [How to log uncaught exceptions in C#](https://betterstack.com/community/questions/how-to-log-uncaught-exceptions-in-csharp/)
+ [Logging in Microservices: 5 Best Practices](https://betterstack.com/community/guides/logging/logging-microservices/)
  + https://opentelemetry.io/
  + https://zipkin.io/
  + https://www.jaegertracing.io/
  
# Automation (Tự động hóa)
+ **Tự động tạo GitHub Repo kèm Source Code và đẩy lên GitHub** sử dụng **GitHub PAT**
+ [Create-GitHub-Repo.ps1 (vẫn phải sửa đường dẫn gốc)](https://github.com/gtechsltn/LoggingWithSerilog/blob/master/Src/LoggingWithSerilog/Create-GitHub-Repo.ps1)
+ [**Tự động tạo Console App Template**](https://github.com/gtechsltn/ConsoleApp)
  + Generate ConsoleApp1 with Log4net, CsvHelper, Dapper, Dapper.Contrib, Newtonsoft.Json, System.Data.SQLite, EntityFramework, SQL Server + Connection String
+ **Tự động triển khai lên IIS với HTTPS Binding** và **IIS Express Development Certificate**
+ [DeployToIIS.ps1 (vẫn phải sửa đường dẫn gốc)](https://github.com/gtechsltn/LoggingWithSerilog/blob/master/Src/LoggingWithSerilog/DeployToIIS.ps1)
+ Tự động tạo bản Deploy sử dụng **MSBuild** với Release mode trong **Visual Studio 2022 Enterprise**
+ [BuildAndCopy.ps1 (vẫn phải sửa đường dẫn gốc)](https://github.com/gtechsltn/TSDataMigration/blob/master/BuildAndCopy.ps1)
+ **Tự động đóng gói vào tệp .zip** để chuẩn bị chuyển giao cho bộ phận **DevOps**
+ [ZipPackage.ps1 (vẫn phải sửa đường dẫn gốc)](https://github.com/gtechsltn/TSDataMigration/blob/master/ZipPackage.ps1)
+ Tự động triển khai lên **Windows Service (services.msc)** với tài khoản Windows (user: MANH\ADMIN, pass: Abc@123$)
+ [BuildAndDeploy.ps1 (vẫn phải sửa đường dẫn gốc)](https://github.com/gtechsltn/TSDataMigration/blob/master/BuildAndDeploy.ps1)

# Referecnes
+ https://betterstack.com/community/guides/logging/logging-best-practices/
+ https://betterstack.com/community/guides/logging/best-dotnet-logging-libraries/
+ https://betterstack.com/community/guides/logging/how-to-start-logging-with-log4net/
+ https://betterstack.com/community/guides/logging/how-to-start-logging-with-serilog/
