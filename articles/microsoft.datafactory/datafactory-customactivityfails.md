<properties 
	pageTitle="Custom .NET activity fails" 
	description="My custom activity does not work as expected or crashes." 
	service="microsoft.datafactory" 
    resource="customactivity"
    authors="spelluru"
    displayOrder="5"
    selfHelpType="generic"
/>

# My custom activity does not work as expected or crashes

## Recommended steps

Debugging consists of a few basic techniques:

1.	If the input slice is not set to **Ready**, confirm that the input folder structure is correct and the input files exists in the input folders. 
2.	In the **Execute** method of your custom activity, use the **IActivityLogger** object to log information that will help you troubleshoot issues. The logged messages will show up in the user log files (one or mote files named: user-0.log, user-1.log, user-2.log, etc...). 

	In the **OutputDataset** blade, click on the slice to see the **DATA SLICE** blade for that slice. You will see **activity runs** for that slice. You should see one activity run for the slice. If you click Run in the command bar, you can start another activity run for the same slice. 

	When you click the activity run, you will see the **ACTIVITY RUN DETAILS** blade with a list of log files. You will see logged messages in the user_0.log file. When an error occurs, you will see three activity runs because the retry count is set to 3 in the pipeline/activity JSON. When you click the activity run, you will see the log files that you can review to troubleshoot the error. 

	In the list of log files, click the **user-0.log**. In the right panel are the results of using the **IActivityLogger.Write** method. If you don't see all messages, check if you have more log files named: user_1.log, user_2.log etc.... Otherwise, the code may have failed after the last logged message.

	You should also check **system-0.log** for any system error messages and exceptions.

3.	Include the **PDB** file in the zip file so that the error details will have information such as **call stack** when an error occurs.
4.	All the files in the zip file for the custom activity must be at the **top level** with no sub folders.
5.	Ensure that the **assemblyName** (MyDotNetActivity.dll), **entryPoint**(MyDotNetActivityNS.MyDotNetActivity), **packageFile** (customactivitycontainer/MyDotNetActivity.zip), and **packageLinkedService** (should point to the Azure blob storage that contains the zip file) are set to correct values. 
6.	If you fixed an error and want to reprocess the slice, right-click the slice in the **OutputDataset** blade and click **Run**. 
7.	The custom activity does not use the **app.config** file from your package, so if your code reads any connection strings from the configuration file, it won't work at runtime. The best practice when using Azure Batch is to hold any secrets in a **Azure KeyVault**, use a certificate-based service principal to protect the **keyvault**, and distribute the certificate to Azure Batch pool. The .NET custom activity then can access secrets from the KeyVault at runtime. This is a generic solution and can scale to any type of secret, not just connection string.

	There is an easier workaround (but not a best practice): you can create a new **Azure SQL linked service** with connection string settings, create a dataset that uses the linked service, and chain the dataset as a dummy input dataset to the custom .NET activity. You can then access the linked service's connection string in the custom activity code and it should work fine at runtime.  

## Recommended documents
[Use custom activities in an Azure Data Factory pipeline](https://azure.microsoft.com/en-us/documentation/articles/data-factory-use-custom-activities/)