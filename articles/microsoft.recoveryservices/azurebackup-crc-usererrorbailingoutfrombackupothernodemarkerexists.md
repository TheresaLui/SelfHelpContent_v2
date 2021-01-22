<properties
	pageTitle="usererrorbailingoutfrombackupothernodemarkerexists"
	description="usererrorbailingoutfrombackupothernodemarkerexists"
	infoBubbleText="SQL database does not exist."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbailingoutfrombackupothernodemarkerexists"
	diagnosticScenario="azurebackup-crc-usererrorbailingoutfrombackupothernodemarkerexists"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorBailingOutFromBackupOtherNodeMarkerExists

<!--issueDescription-->
We have identified that your databases is a part of Always on Availability Group, Backup was successful on one of the node from the same Availability Group.
<!--/issueDescription-->

## **Recommended Steps**

1. In case of databases which are part of Always on Availability Group, both the Primary and the Secondary nodes are capable of taking log backups.
1. By default Azure Workload Backup triggers the backup request on all the nodes of AG and checks for the Backup preference of the Always on Availability group. 
1. In case the Backup Preference of the Always on Availability group is Prefer Secondary or Any Replica, all the nodes (Primary and multiple secondaries) will compete to take the log backups but at the end only one of the nodes proceeds with the log backup for the database. 
1. This is decided internally by Azure Workload Backup by stimulating a lock based mechanism between the AG nodes. The node which successfully takes the lock proceeds with the backup and the backup task on rest of the nodes fails with UserErrorBailingOutFromBackupOtherNodeMarkerExists.
