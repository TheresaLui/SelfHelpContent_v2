<properties
	pageTitle="Troubleshoot AzCopy"
	description="Troubleshoot AzCopy"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a6549db8-4311-465a-92d0-a5eab450649d"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Troubleshoot AzCopy 

1. AzCopy creates log and plan files for every job. You can use the logs to investigate and troubleshoot any potential problems. 
2. This article helps you to perform advanced configuration tasks and helps you to troubleshoot issues that can arise as you use AzCopy. 
3. The logs will contain the status of failure (UPLOADFAILED, COPYFAILED, and DOWNLOADFAILED), the full path, and the reason of the failure. 
4. By default, the log and plan files are located in the %USERPROFILE%\.azcopy directory on Windows or $HOME$\.azcopy directory on Mac and Linux, but you can change that location if you want. 

## Recommended Documents

[Use AzCopy Configure](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-configure)

