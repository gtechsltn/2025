# Tech Notes on 2025

# Updated on 2025-09-18

### Chuẩn hóa tài liệu .md
https://github.com/gtechsltn/FileReplacer

### So sánh đầu ra của 2 lần chạy ở 2 branch (master và hotfix/SG)
https://github.com/gtechsltn/FolderCompare

### Tạo tệp đầu vào cho Data Export tool (xóa log, xóa bagit, chạy script reset db, tạo tệp input.csv, sửa connection string ở D:\ThirdSight\ThirdSight.DataMigration1\TSDataExport.exe.config)
https://github.com/gtechsltn/CsvGenerator

### Tìm lỗi nếu có trên toàn bộ tệp log ở thư mục D:\ThirdSight\logs\ThirdSight.DataMigration1
https://github.com/gtechsltn/SearchText

# Tech Notes on 2025
+ [EF4TS (HAY HAY HAY HAY HAY)](https://github.com/gtechsltn/EF4TS)
+ [EFCoreConsole](https://github.com/gtechsltn/EFCoreConsole)
+ [EFSeederTool (HAY HAY HAY HAY HAY)](https://github.com/gtechsltn/EFSeederTool)
+ [EFCoreSeedDataGenerator](https://github.com/gtechsltn/EFCoreSeedDataGenerator)
+ [WebBanHang (HAY HAY HAY HAY HAY)](https://github.com/gtechsltn/WebBanHang)
+ [Tool Exec SQL Files (Batch processing + Parallel processing) (HAY HAY HAY HAY HAY)](https://github.com/gtechsltn/AdoNetExecSQLFiles)
+ [Tool Exec SQL Files (ChatGPT)](https://chatgpt.com/c/689aa0b9-92e0-8321-8a25-a350188e6767)
+ [ConsoleCleanArch](https://github.com/gtechsltn/ConsoleCleanArch)
+ [Enterprise_WebAPI_Starter_Kit (HAY HAY HAY)](https://github.com/gtechsltn/Enterprise_WebAPI_Starter_Kit)
+ [Clean Architecture Blazor UI](https://docs.google.com/document/d/1PG0b_OrXPl97URJXEQjVn2I0hmaNLyCCQlp3NnWO0nQ)
+ [UserInfoMgmt (2025-Aug-04)](https://github.com/gtechsltn/UserInfoMgmt)
+ [FluentBlazorCrudApp (2025-Aug-05)](https://github.com/gtechsltn/FluentBlazorCrudApp)
+ [DBToWordPDF or SqlDbExporter](https://github.com/gtechsltn/DBToWordPDF)
+ [ClosedXML](https://github.com/gtechsltn/ClosedXML)
+ [Windows Console Application (C#) vs Windows Service (C#)](https://github.com/gtechsltn/CsvPdfWatcherService)
+ [CsvReaderUI](https://github.com/gtechsltn/CsvReaderUI)
+ [Service-Oriented Architecture](https://docs.google.com/document/d/1RsFfJ-Bd-7FohgN-FXs4bKiI8BowZeAgHvQK_SKDBM8)
+ [Library Management System](https://github.com/gtechsltn/LibMgmtSys)
  + D:\gtechsltn\LibMgmtSys\Src\LMS\Program.cs
+ [HTML5](https://github.com/gtechsltn/HTML5-API-Paste-Image-From-Clipboard)
+ [**Auto DAL Code Genration from Stored Procedures**](https://github.com/gtechsltn/Auto-DAL-Code-Generation-From-StoredProcedures)
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

# .NET Framework 4.8
+ OpenAI ChatGPT
+ Google Gemini
+ .NET Framework 4.8
+ Console App (C#)
+ CommandLineParser 2.9.1
+ Newtonsoft.Json 13.0.3
+ CsvHelper 33.1.0
+ log4net 3.1.0
+ Dapper 2.0.78
+ Dapper.Contrib 2.0.78
+ [CommandDefinition Structure](https://www.lluisfranco.com/dapper-how-to-change-commanddefinition-parameters-values/)
+ [CommandTimeout](https://github.com/gtechsltn/SPInsertData/blob/master/Opt2.CreateTestData/Program.cs)
+ [Program.cs](https://github.com/gtechsltn/SPInsertData/blob/master/Opt2/Program.cs)
+ [DapperConfig.Initialize();](https://github.com/gtechsltn/SPInsertData/blob/master/Opt2.CreateTestData/Program.cs#L35)
+ [DapperConfig.Initialize(){}](https://github.com/gtechsltn/SPInsertData/blob/master/Opt2.CreateTestData/Program.cs#L529)
+ [SPInsertData](https://github.com/gtechsltn/SPInsertData)
+ [SQL-JSON](https://github.com/gtechsltn/SQL-JSON)
+ TVP and Stored Procedure

## Step 1: SQL Server – Define Table Type
```
CREATE TYPE dbo.TVP_Workspace AS TABLE
(
    WkSpcID BIGINT,
    MetaJson NVARCHAR(MAX)
);
```

## Step 2: SQL Server – Stored Procedure
```
CREATE PROCEDURE dbo.InsertMetaWorkspaces
    @Workspaces dbo.TVP_Workspace READONLY
AS
BEGIN
    INSERT INTO meta_workspaces (WkSpcID, meta_json)
    SELECT WkSpcID, MetaJson FROM @Workspaces;
END
```

## Step 3: C# – Create DataTable for TVP
```
private static DataTable CreateWorkspaceTvp(IEnumerable<MetaWorkspace> workspaces)
{
    var table = new DataTable();
    table.Columns.Add("WkSpcID", typeof(long));
    table.Columns.Add("MetaJson", typeof(string));

    foreach (var ws in workspaces)
    {
        table.Rows.Add(ws.WkSpcID, ws.MetaJson);
    }

    return table;
}
```

## Step 4: Dapper – Call Stored Procedure with CommandDefinition
```
using (var connection = new SqlConnection(connectionString))
{
    var workspaces = new List<MetaWorkspace>
    {
        new MetaWorkspace { WkSpcID = 1, MetaJson = "{ \"a\": 1 }" },
        new MetaWorkspace { WkSpcID = 2, MetaJson = "{ \"b\": 2 }" }
    };

    var tableParam = new SqlParameter("@Workspaces", CreateWorkspaceTvp(workspaces))
    {
        SqlDbType = SqlDbType.Structured,
        TypeName = "dbo.TVP_Workspace"
    };

    var command = new CommandDefinition(
        commandText: "dbo.InsertMetaWorkspaces",
        parameters: new { }, // we'll inject via DynamicParameters
        commandType: CommandType.StoredProcedure,
        commandTimeout: 60
    );

    var dynamicParams = new DynamicParameters();
    dynamicParams.Add("@Workspaces", tableParam.Value, DbType.Object, ParameterDirection.Input);

    // You can also pass SqlParameter directly via ADO.NET
    connection.Execute(command.CommandText, dynamicParams, commandType: command.CommandType);
}
```

# Backend Development:
+ [.NET Framework 4.8](https://github.com/gtechsltn/BackendNetFw48)
+ [.NET 8](https://github.com/gtechsltn/BackendNet8)

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

```
Solution for the coursera course Service-Oriented Architecture offered by University of Alberta
https://github.com/gtechsltn/Service-Oriented-Architecture

SOA module of a larger web portal. This module pertains to data warehousing and analysis, logging and advertisement services.
https://github.com/markus-lamm/hv-sos100-dataservice
https://github.com/gtechsltn/hv-sos100-dataservice

This project contains prototype for SQL IDE developed as my course project for 3rd year of studies in kpi. Technologies: C#, WPF, PostgreSQL
https://github.com/mynameiszp/sql-ide-project/tree/main
https://github.com/gtechsltn/sql-ide-project

✅ MVC 5, Bootstrap, Web API 2, JQuery, Ajax, EF6, DDD
https://github.com/piotr-mamenas/performance-app
https://github.com/gtechsltn/performance-app

WEB API in .Net 7 with JWT Auth and EF Core. Ths is a Web API project for Authentication and Authorization. It used ASP.Net Core 7 using EF Core with MS SQL DB.
https://github.com/ahsan-javied/Web-API-Dot-Net-Core-7
https://github.com/gtechsltn/Web-API-Dot-Net-Core-7

Northwind + AgularJS
https://github.com/alisuleymantopuz/soa-arch
https://github.com/gtechsltn/soa-arch

Northwind Backend (.NET Core 3.1)
This service oriented architecture project was developed on .NET Core.
https://github.com/gtechsltn/NorthwindBackend

Document Management System

https://github.com/diaakhateeb/FRISS_DocumentManagementSystem
https://github.com/gtechsltn/FRISS_DocumentManagementSystem

ASP.NET WCF, MySQL

A SOAP-based loan management system built with C# and ASP.NET WCF, designed to streamline library operations with CRUD functionalities for loans, user-friendly integration, and scalable service-oriented architecture.

https://github.com/Yassinekrn/SOAP-Based-Loan-Management-WS
https://github.com/gtechsltn/SOAP-Based-Loan-Management-WS

Service-Oriented Architecture
https://github.com/KountourisPanagiotis/products-soa-app
https://github.com/gtechsltn/products-soa-app

ShowCase: QuestionController
https://github.com/cloudtoid/poem/blob/master/showcase/QnA/Controllers/QuestionController.cs

Mini e-shop MVC project (.NET 6)
https://github.com/ResadMemmedov0035/MiniEshopOnionDemo
https://github.com/gtechsltn/MiniEshopOnionDemo

Error Handlers
https://github.com/ResadMemmedov0035/MiniEshopOnionDemo/blob/master/MiniEshop.Web/Controllers/ErrorHandleController.cs

Background File Processing Service (.NET 8)
https://github.com/Voidcoolis/CvsProcessorAPI
https://github.com/gtechsltn/CvsProcessorAPI

This API simulates a real-world background file processing service. CSV files uploaded by authenticated users are queued and processed line by line using a background service. This architecture showcases common backend engineering patterns.
https://github.com/gtechsltn/CvsProcessorAPI/blob/master/CvsProcessorAPI/Queue/InMemoryFileProcessingQueue.cs

Queue
System.Collections.Concurrent
ConcurrentQueue<string>
IFileProcessingQueue
Enqueue
Dequeue
```

# ThirdSight-SLA-PreCheck (ThirdSight.SLA.PreCheck)
+ [ThirdSight-SLA-GetUniqueFileRefNum](https://diskstation2:3000/manh.nguyen/ThirdSight-SLA-GetUniqueFileRefNum)
+ [Rename-Replace](https://github.com/gtechsltn/Rename-Replace)
+ [ThirdSight-SLA-PreCheck](https://diskstation2:3000/manh.nguyen/ThirdSight-SLA-PreCheck)
