<properties
	pageTitle="ExtensionCommandExecFailure"
	description="ExtensionCommandExecFailure"
	infoBubbleText="Extension command execution failure"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
  	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-extensioncommandexecfailure"
	diagnosticScenario="azurebackup-crc-extensioncommandexecfailure"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionCommandExecFailure

<!--issueDescription-->
## We have identified that your backup operation failed because of the extension state.
<!--/issueDescription-->

## **Recommended Steps**
To resolve ExtensionCommandExecFailure issue perform the below:

* Update Reg-key value, run the below command from elevated (as administrator) command-prompt: <br/>

	`REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgent" /v IsProviderInstalled /t REG_SZ /d False /f`

* Rename the  C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.WindowsAzure.Storage to C:\Windows\Microsoft.NET\assembly\GAC_MSIL\Microsoft.WindowsAzure.Storage.old
* Triggered a manual backup
