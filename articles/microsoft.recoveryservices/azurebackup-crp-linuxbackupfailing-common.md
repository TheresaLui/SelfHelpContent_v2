<properties
	pageTitle="Backup of Azure virtual machine fails"
	description="Backup of Azure virtual machine fails"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637320"
	resourceTags=""
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="fe4213e1-5c21-455d-9b16-3089ccf8dc81"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup - Backup is failing for my VM

## **Recommended Steps**
- For **UserErrorGuestAgentStatusUnavailable** issue ensure the Azure VM Guest Agent is in Ready state by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2107408) <br>
- For **UserErrorVmProvisioningStateFailed** issue verify and ensure VM provisioning state is in Succeeded state by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2112897) <br>
- For **GuestAgentSnapshotTaskStatusError** issue ensure VM Agent status is healthy and extension is able to execute snapshots by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2112898) <br>
- [If your Linux OS/Kernel version is not listed here, then it is not supported](https://go.microsoft.com/fwlink/?linkid=2112798)<br>

## **Recommended Documents**
- For troubleshooting Azure VM Backup issues, refer to the [troubleshooting article](https://go.microsoft.com/fwlink/?linkid=2113100)
- For list of common Azure VM Backup error codes, refer to this [article](https://go.microsoft.com/fwlink/?linkid=2112917)




