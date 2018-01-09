<properties
	pageTitle="Backup of Linux Azure virtual machine fails"
	description="Linux VM Snapshot issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Backup of Linux Azure virtual machine fails

## **Recommended steps**
To resolve common isuess, try one or more of the following steps.

**VM agent is unable to communicate with the Azure Backup Service?** <br>
If your Azure Linux VMs are failing with this error on or after Jan 4th, 2018, run the below command on the affected VMs and retry the backups
` sudo rm -f /var/lib/waagent/*.[0-9]*.xml `

Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot1) to resolve communication issues <br>

**Snapshot operation failed due to no network connectivity on the virtual machine?** <br>
Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot2) to resolve snapshot failure issues <br>

**VMSnapshot extension operation failed?**<br>
This issue may occur if extensions cannot be loaded, Backup fails because a snapshot cannot be taken.<br>
Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot3) to resolve extension operation failed issues.b

**Unable to perform the operation as the VM Agent is not responsive?**<br>
This issue may occur if the VM Agent might have been corrupted or the service might have been stopped. Follow the [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot4) to resolve this issue.<br>

**Backup failed with an internal error - Please retry the operation in a few minutes. If the problem persists, contact Microsoft Support?**<br>
Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot5) to resolve theses issues


## **Recommended documents**
[Azure virtual machine backup troubleshooting guide](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)<br>
