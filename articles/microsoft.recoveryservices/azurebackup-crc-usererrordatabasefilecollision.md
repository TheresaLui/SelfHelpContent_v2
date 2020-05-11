<properties
	pageTitle="UserErrorDatabaseFileCollision"
	description="UserErrorDatabaseFileCollision"
	infoBubbleText="The database has several data files and some of the files with same name already exist on the destination server."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrordatabasefilecollision"
	diagnosticScenario="azurebackup-crc-usererrordatabasefilecollision"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorDatabaseFileCollision

<!--issueDescription-->
We have identified that database recovery failed because some of data files that you are trying to restore already exist (with the same name) on the destination server.
<!--/issueDescription-->

## **Recommended Steps**

During ALR (Alternate Location Recovery), you specify the target file path for recovery. If the path specified contains data files (with extensions .mdf, .ldf and .ndf) with the same name as the ones that you are trying to restore, then it the restore will fail. You can verify this by checking specified file name from **Advanced Configuration** blade. 

To resolve this issue, change the name of the target file (with the extension .mdf, .ldf or .ndf) to prevent file name conflicts.

**Note**: If renaming is not an option and you want the target files to be replaced, then choose the option ALR with overwrite.   
