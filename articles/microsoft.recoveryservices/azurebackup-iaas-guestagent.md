<properties
	pageTitle="Diagnose and resolve issues with Azure Virtual Machine Windows Guest Agent"
	description="Diagnose and resolve issues with Azure Virtual Machine Windows Guest Agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684549"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1f35691a-9c9f-4176-add6-52866f441644"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues with Azure Virtual Machine Windows Guest Agent

## **Recommended Steps**
Your backup operation will fail with *UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup* if the Azure VM Guest Agent is not in **Ready** state. To resolve this issue: 
-  Open *Azure Portal > VM > Settings > Properties blade > agent status* and check if it is **Ready**. If not check whether the *Windows Azure Guest Agent* service is running in the VM services (using services.msc). Try to restart the *Windows Azure Guest Agent* service and retry the backup operation (try an ad-hoc backup). For steps to restart the agent, see [Windows VMs](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-but-unresponsive-for-windows-vms) or [Linux VMs](https://docs.microsoft.com/azure/virtual-machines/linux/update-agent).
-  If *Windows Azure Guest Agent* service does not restart, then [download](https://go.microsoft.com/fwlink/?LinkID=394789&clcid=0x409), reinstall the agent, ensure it is in **Ready** state and retry the backup operation. 

## **Recommended Documents**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://go.microsoft.com/fwlink/?linkid=2107408)
- [Install the VM agent](https://go.microsoft.com/fwlink/?linkid=2107314)
- [The agent is installed in the VM, but it's unresponsive](https://go.microsoft.com/fwlink/?linkid=2107410)
