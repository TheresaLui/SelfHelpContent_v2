<properties
	pageTitle="Azure Backup - Backup is failing for my VM"
	description="Azure Backup - Backup is failing for my VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637320"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="ac1e1f73-2210-434a-8057-cdee9863085d"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup - Backup is failing for my VM

## **Recommended Steps**
- For **UserErrorGuestAgentStatusUnavailable** issue ensure the Azure VM Guest Agent is in Ready state by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2107408) <br>
- For **UserErrorVmProvisioningStateFailed** issue verify and ensure VM provisioning state is in Succeeded state by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2112897) <br>
- For **GuestAgentSnapshotTaskStatusError** issue ensure VM Agent status is healthy and extension is able to execute snapshots by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2112898) <br>

## **Recommended Documents**
- For troubleshooting Azure VM Backup issues, refer to the [troubleshooting article](https://go.microsoft.com/fwlink/?linkid=2113100)
- For list of common Azure VM Backup error codes, refer to this [article](https://go.microsoft.com/fwlink/?linkid=2112917)
