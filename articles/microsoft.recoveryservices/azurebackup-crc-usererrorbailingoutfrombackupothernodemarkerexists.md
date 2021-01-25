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
We have identified that your databases is a part of Always on Availability Group. Backup was successful on one of the nodes from the same Availability Group.
<!--/issueDescription-->

## **Recommended Steps**

1. Databases in the Always on Availability Group have Primary and the Secondary nodes, which are capable of taking log backups.
1. By default, Azure Workload Backup triggers the backup request on all nodes of Availability Group (AG). It also checks for the Backup preference of the Always on Availability group. 
1. If the Backup Preference of the Always on Availability group is set to **Prefer Secondary or Any Replica**, all nodes (Primary and multiple secondaries) compete to take the log backups. Ultimately, only one node will proceed with the log backup for the database. 
1. To determine which node will proceed with the log backup, Azure Workload Backup stimulates a lock-based mechanism between the AG nodes. The node that successfully takes the lock proceeds with the backup. On the remaining nodes, the backup task fails with "UserErrorBailingOutFromBackupOtherNodeMarkerExists".
