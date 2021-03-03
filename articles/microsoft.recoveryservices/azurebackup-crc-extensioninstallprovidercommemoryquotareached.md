<properties
	pageTitle="extensioninstallprovidercommemoryquotareached"
	description="extensioninstallprovidercommemoryquotareached"
	infoBubbleText="extension could not be installed"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-extensioninstallprovidercommemoryquotareached"
	diagnosticScenario="azurebackup-crc-extensioninstallprovidercommemoryquotareached"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionInstallProviderCOMMemoryQuotaReached

<!--issueDescription-->
We have identified that your backup operation failed because the extension could not be installed.  
<!--/issueDescription-->

## **Recommended steps**

To resolve this issue,
- On the impacted machine, open the Registry Editor:<br>
   open Run window and type 'regedit'
- Navigate to the **HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Session Manager\SubSystems - windows**
- Right-click on Windows shared section and click 'Modify'.
- Update the value with Windows SharedSection=1024,20480,4096.
- Once the registry is updated, reboot the server and retry the backup operation.

>**Note:** Restarting server can have an impact on your production environment. Make sure to follow the approval process and restart the server at the scheduled downtime.
