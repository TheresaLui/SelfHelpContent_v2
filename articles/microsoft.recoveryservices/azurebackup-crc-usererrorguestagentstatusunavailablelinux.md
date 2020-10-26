<properties
	pageTitle="User Error Guest Agent Status Unavailable: Linux"
	description="User Error Guest Agent Status Unavailable: Linux"
	infoBubbleText="VM agent unable to communicate with Azure Backup"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorguestagentstatusunavailablelinux"
	diagnosticScenario="azurebackup-crc-usererrorguestagentstatusunavailablelinux"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# User Error Guest Agent Status Unavailable: Linux

<!--issueDescription-->
We have identified that your backup operation might have failed, because the backup service was unable to communicate with your VM's Guest Agent.
<!--/issueDescription-->

## **Recommended Steps**

4 out of 5 customers resolved their backup failures by following these steps:

Step 1: Check if the [OS is of supported version](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)<br>
Step 2: Check the agent status and restart the agent service on the VM. Ensure latest version of the agent is installed and trigger a on-demand backup. Learn how to verify agent status for [Ubuntu](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent#ubuntu); [Red Hat / CentOS](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent#red-hat--centos); [RHEL/CentOS 7](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent#rhelcentos-7); [SUSE SLES](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent#suse-sles); [Debian](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent#debian); [Oracle Linux 6 and Oracle Linux 7](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent#oracle-linux-6-and-oracle-linux-7)<br>
Step 3: Check if the root drive has enough space
