<properties
	pageTitle="Backup of Windows Azure virtual machine fails"
	description="Top issues causing Windows Azure virtual machine backup failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Backup of Windows Azure virtual machine fails

## **Recommended steps**
To resolve common issues, try one or more of the following steps.

**VM agent is unable to communicate with the Azure Backup Service?** <br>
Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot1) to resolve communication issues <br>

**Snapshot operation failed due to no network connectivity on the virtual machine?** <br>
Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot2) to resolve snapshot failure issues <br>

**VMSnapshot extension operation failed?**<br>
This issue may occur if extensions cannot be loaded, Backup fails because a snapshot cannot be taken.<br>
Follow these [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot3) to resolve extension operation failed issues.

**Unable to perform the operation as the VM Agent is not responsive?**<br>
This issue may occur if the VM Agent might have been corrupted or the service might have been stopped. Follow the [troubleshooting steps](https://aka.ms/iaasvmbackuptshoot4) to resolve this issue.<br>



## **Recommended documents**
[Azure virtual machine backup troubleshooting guide](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)<br>
