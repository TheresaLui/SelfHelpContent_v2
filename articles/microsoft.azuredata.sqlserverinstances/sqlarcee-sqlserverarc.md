<properties
	pageTitle="SQL Server - Azure Arc"
	description="SQL Server - Azure Arc"
	infoBubbleText="SQL Server - Azure Arc"
	service="microsoft.azuredata"
	resource="sqlserverinstances"
	ms.author="amigan,ujpat,amamun"
	displayOrder=""
	articleId="d534114a-5bef-433d-b3e1-0e3bf098d90f"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748837,32748843,32748839,32748841"
	resourceTags=""
	productPesIds="17126"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	ownershipId="AzureData_SQL_Server_Azure_Arc"
/>

# SQL Server - Azure Arc

Most users are able to resolve their issues with SQL Server - Azure Arc using the recommended documents below.

## **Recommended Steps**

- Before you can install SQL Server Azure Arc Resource, please make sure you follow the below pre-requisites: 

   - Your machine is on-boarded to Arc for Servers. 
   - Your machine has SQL Server (2008+?) installed.  
   - Machine/SQL instance onboarding performed via a script running on the target machine, which is configured to use the latest PowerShell with Azure module installed on Windows. The user authenticates with Azure in PowerShell before running the script. 
   - .NET 4.7.2 or later may be required depending on the windows version. 

 

- TLS 1.2 may need to be enabled first. Most of the issues are fixed by following the below script: 

     ```SQL
    [Net.ServicePointManager]::SecurityProtocol` = [Net.SecurityProtocolType]::Tls12  

    Install-PackageProvider -Name NuGet -MinimumVersion 2.8.5.201 -Force  

    Register-PSRepository -Default  

    Install-Module -Name Az –AllowClobber 

    Update-Module Az 
     ```
 

- In case a resource cannot be created/updated/removed/accessed, a standard error message will be provided by the Azure infrastructure. 
- Users can create Tags on Azure Arc Resource only after the resource is created. 
- Currently you do not have any option to unregister the SQL Arc resource. You can delete the arc resource by navigating to All Resources on Azure Portal. 
- If you try to download and run any script from the target machine’s browser directly, then you may receive an error indicating the script is not signed  

  To fix this, you May need to bypass execution policy (Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass) or save the script file locally first, copy-paste the content and run it manually. 