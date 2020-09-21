<properties
    pageTitle="How to questions: Client drivers and API"
    description="How to questions: Client drivers and API"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745424"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="BD3444BA-588A-4766-B87E-0B2AAFA8D6EE"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Client drivers and API

### Client Drivers
Azure SQL Service supports multiple [client drivers](https://docs.microsoft.com/sql/connect/sql-connection-libraries?WT.mc_id=pid:13491:sid:32745424&view=sql-server-ver15) that your applications can use for interacting with the SQL database. These drivers are available for a variety of programming languages, running on Windows, Linux or macOS.

### APIs
You can build applications using the language and API of choice, as Azure SQL supports various languages and frameworks including relational, JSON, spatial and XML data.  Applications written in an object-oriented programming language often use SQL drivers, which return queried data in a relational format (e.g., C# using ADO.NET SQL driver, C++ using ODBC).  Another popular choice is object relational mapping, which uses classes defined to match the data columns of particular SQL tables. The driver performs the object-relational mapping (ORM) to return queried data as an instance of a class (e.g., Microsoft's Entity Framework (EF) for C#, and Hibernate for Java).

## **Recommended Documents**  

- [Azure SQL Database APIs for .NET](https://docs.microsoft.com/dotnet/api/overview/azure/sql?WT.mc_id=pid:13491:sid:32745424&view=azure-dotnet#overview)
- [Azure SQL Database APIs for Java](https://docs.microsoft.com/java/api/overview/azure/sql?WT.mc_id=pid:13491:sid:32745424&view=azure-java-stable#overview)
