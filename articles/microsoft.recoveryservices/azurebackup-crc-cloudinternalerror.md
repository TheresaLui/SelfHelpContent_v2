<properties
	pageTitle="CloudInternalError"
	description="CloudInternalError"
	infoBubbleText="Microsoft Azure Backup encountered an internal error. (ID: 130001)"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cloudinternalerror"
	diagnosticScenario="azurebackup-crc-cloudinternalerror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CloudInternalError

<!--issueDescription-->
We have identified that backup operation failed due to an underlying storage issue or outdated agent.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, try the following: 

* Ensure backup agent is latest by following these [steps](https://go.microsoft.com/fwlink/?linkid=229525&clcid=0x409)
* Check if there are any storage issues, resolve them, and retry the backup operation
