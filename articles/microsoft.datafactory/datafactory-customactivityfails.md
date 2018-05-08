<properties 
	pageTitle="Custom .NET activity fails" 
	description="My custom activity does not work as expected or crashes." 
	service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="5"
    selfHelpType="resource"
	cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>

# My custom activity does not work as expected or crashes

## **Recommended steps**

Debugging consists of a few basic techniques:

1.	If the input slice is not set to **Ready**, confirm that the input folder structure is correct and the input files exists in the input folders. 
2.	In the **Execute** method of your custom activity, use the **IActivityLogger** object to log information that will help you troubleshoot issues. The logged messages will show up in the user log files (one or mote files named: user-0.log, user-1.log, user-2.log, etc...).	
3.	Include the **PDB** file in the zip file so that the error details will have information such as **call stack** when an error occurs.
4.	All the files in the zip file for the custom activity must be at the **top level** with no sub folders.
5.	Ensure that the **assemblyName** (MyDotNetActivity.dll), **entryPoint**(MyDotNetActivityNS.MyDotNetActivity), **packageFile** (customactivitycontainer/MyDotNetActivity.zip), and **packageLinkedService** (should point to the Azure blob storage that contains the zip file) are set to correct values. 
6.	If you fixed an error and want to reprocess the slice, right-click the slice in the **OutputDataset** blade and click **Run**. 
7.	The custom activity does not use the **app.config** file from your package, so if your code reads any connection strings from the configuration file, it won't work at runtime. The best practice when using Azure Batch is to hold any secrets in a **Azure KeyVault**, use a certificate-based service principal to protect the **keyvault**, and distribute the certificate to Azure Batch pool. The .NET custom activity then can access secrets from the KeyVault at runtime. This is a generic solution and can scale to any type of secret, not just connection string.

## **Recommended documents**
[Use custom activities in an Azure Data Factory pipeline](https://docs.microsoft.com/azure/data-factory/v1/data-factory-use-custom-activities/)