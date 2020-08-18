<properties
	pageTitle="Database Backup Failure with Differential Backup Error"
	description="Database Backup Failure with Differential Backup Error"
	infoBubbleText="Database Backup Failure with Differential Backup Error"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder=""
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="afb2f7b4-2b25-45ce-8f36-8631274e99cf-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The error/symptom indicates you have configured Snapshots backup at VM level which by default does not do a copy only backup resulting in breaking the LSN chain for your native backups configured on your SQL Server.
<!--/issueDescription-->

## **Recommended Steps**

- To make sure that the native backups don’t get impacted due to other backup applications making LSN updates you can take [COPYONLY](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Furldefense.proofpoint.com%2Fv2%2Furl%3Fu%3Dhttps-3A__nam06.safelinks.protection.outlook.com_-3Furl-3Dhttps-253A-252F-252Fdocs.microsoft.com-252Fen-2Dus-252Fsql-252Frelational-2Ddatabases-252Fbackup-2Drestore-252Fcopy-2Donly-2Dbackups-2Dsql-2Dserver-253Fview-253Dsql-2Dserver-2Dver15-26data-3D02-257C01-257CPedro.Faro-2540microsoft.com-257C24d50b2d34504df854ea08d7bb905589-257C72f988bf86f141af91ab2d7cd011db47-257C1-257C0-257C637184100936755560-26sdata-3DZp72GC1oDfvnvQCXNwDXGOepUtDV2-252BpA8MVSCTnAQng-253D-26reserved-3D0%26d%3DDwMFAw%26c%3DeIGjsITfXP_y-DLLX0uEHXJvU8nOHrUK8IrwNKOtkVU%26r%3DMgr2uqOk6h1UfEpzHn6sE-sS_VBRFfopydtFN_0IEPI%26m%3DeVofNIT9Eh3JGfs64QbzGaXf50Vtt7zl2JmnAXS5v4Y%26s%3DqETVLw2fU0vosXzM5mqzbifDKG5i5xd9AVNCYG7o6fE%26e%3D&data=02%7C01%7CUjjwal.Patel%40microsoft.com%7C766059f7bf1a4dfe4c1c08d7d023b3b8%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637206724120117770&sdata=wQP1M8GQ%2Fk7aIWfmHIkZz7Ai0XuegfCT8Y9shHPMAIU%3D&reserved=0) backups. The copy only backups would not cause impact on LSN of the native backups.
-  To fix this issue, add the following registry keys on each of the VMs hosting SQL server instances and where VM backups are configured and post adding this registry key the native backups should not fail.	
```[HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\BCDRAGENT] "USEVSSCOPYBACKUP"="TRUE"```

## **Recommended Documents**

* [Troubleshoot VM snapshot issues](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues)


