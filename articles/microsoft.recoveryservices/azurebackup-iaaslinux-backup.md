<properties
	pageTitle="Backup of Linux Azure virtual machine fails"
	description="Linux VM Snapshot issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="493a4d5a-add2-4831-abc4-7352a51b60d2"
	ownershipId="StorageMediaEdge_Backup"
/>

# Backup of Linux Azure Virtual Machine fails

## **Recommended Steps**
- For **UserErrorGuestAgentStatusUnavailable** issue ensure the Azure VM Guest Agent is in Ready state by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2107408) <br>
- For **UserErrorVmProvisioningStateFailed** issue verify and ensure VM provisioning state is in Succeeded state by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2112897) <br>
- For **GuestAgentSnapshotTaskStatusError** issue ensure VM Agent status is healthy and extension is able to execute snapshots by following these [troubleshooting steps](https://go.microsoft.com/fwlink/?linkid=2112898) <br>
- [If your Linux OS/Kernel version is not listed here, then it is not supported](https://go.microsoft.com/fwlink/?linkid=2112798)<br>

## **Recommended Documents**
- For troubleshooting Azure VM Backup issues, refer to the [troubleshooting article](https://go.microsoft.com/fwlink/?linkid=2113100)
- For list of common Azure VM Backup error codes, refer to this [article](https://go.microsoft.com/fwlink/?linkid=2112917)

