<properties
	pageTitle="UserErrorAGReplicaRoleIsResolving"
	description="UserErrorAGReplicaRoleIsResolving"
	infoBubbleText="Backup failed as current replica does not have a healthy role."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererroragreplicaroleisresolving"
	diagnosticScenario="azurebackup-crc-usererroragreplicaroleisresolving"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorAGReplicaRoleIsResolving

<!--issueDescription-->
We have identified that your operation failed because during the backup operation the replica role was in Resolving State.
<!--/issueDescription-->

## **Recommended Steps**
This is a transient error. Retry the operation after the failover operation is complete.
