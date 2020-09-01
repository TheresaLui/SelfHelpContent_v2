<properties
	pageTitle="Managed Instance - Azure Arc Administration"
	description="Managed Instance - Azure Arc Administration"
	infoBubbleText="Managed Instance - Azure Arc Administration"
	service="microsoft.azuredata"
	resource="sqlmanagedinstances"
	ms.author="amigan,jopilov,prmadhes"
	displayOrder=""
	articleId="0c3739b5-5d9a-4499-ae1c-2024ba3fa6d9"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32743941"
	resourceTags=""
	productPesIds="17125"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>

# Managed Instance - Azure Arc Administration

Most users are able to resolve their issues with Managed Instance - Azure Arc using the recommended documents below.

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