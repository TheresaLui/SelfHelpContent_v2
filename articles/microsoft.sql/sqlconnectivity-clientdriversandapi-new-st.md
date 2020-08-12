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

Azure SQL Service supports multiple  **Client drivers**  that your applications can use for interacting with the SQL database. These drivers are available for a variety of programming languages, running on Windows, Linux or macOS.

Client programs that are written in an object-oriented programming language often use SQL drivers (**Drivers for relational access**), which return queried data in a format that is more relational than object oriented. (e.g.,  C# using ADO.NET SQL driver, C++ using ODBC).  
And other drivers  (**drivers for object relational mapping**) work by expecting that classes have been defined to match the data columns of particular SQL tables. The driver then performs the object-relational mapping (ORM) to return queried data as an instance of a class (e.g., Microsoft's Entity Framework (EF) for C#, and Hibernate for Java).   

You  can build **APIs** using the language of choice as Azure SQL supports various languages and frameworks. SQL database supports relational, JSON, spatial and XML data.

## **Recommended Documents**  

For questions related to client drivers and how to use for interacting with your database  please refer

- [Connection modules for Microsoft SQL Database](https://docs.microsoft.com/sql/connect/sql-connection-libraries?WT.mc_id=pid:13491:sid:32745424&view=sql-server-ver15)

For configuring and using APIs for your SQL database please refer  
- [Azure SQL Database APIs for .NET](https://docs.microsoft.com/dotnet/api/overview/azure/sql?WT.mc_id=pid:13491:sid:32745424&view=azure-dotnet#overview)
- [Azure SQL Database APIs for Java](https://docs.microsoft.com/java/api/overview/azure/sql?WT.mc_id=pid:13491:sid:32745424&view=azure-java-stable#overview)
