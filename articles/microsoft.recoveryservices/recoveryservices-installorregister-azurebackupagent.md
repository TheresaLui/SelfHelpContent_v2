<properties
	pageTitle="Windows Backup to Azure Backup/Install or register Azure Recovery Services Agent"
	description="Windows Backup to Azure Backup/Install or register Azure Recovery Services Agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="saurabhsensharma"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Windows Backup to Azure Backup/Install or register Azure Recovery Services Agent

## **Recommended steps**
Try the recommended steps below to resolve commonly observed issues with installation or registration of the **Microsoft Azure Recovery Services Agent**

### **Installation**
* Ensure that the user account installing the Azure Recovery Services Agent is a member of the **Local Administrators** group on the server/client or has been granted administrative privileges

* Ensure that the installation directory for Azure Recovery Services Agent does not have the following attributes:<br>
    1. System
    2. Hidden
    3. Compressed
    4. Encrypted

### **Registration**
* Ensure that firewall settings on the Windows server/client with Azure Recovery Services Agent are configured to allow the following URLs: <br>
    1. www.msftncsi.com
    2. *.Microsoft.com
    3. *.WindowsAzure.com
    4. *.microsoftonline.com
    5. *.windows.net

* Ensure that the system clock on the server/client where you install Azure Recovery Services Agent has the correct time for the time zone that the server/client is configured for

* Ensure that .tmp files at **C:\Windows\Temp** directory have been deleted before registration

* If you are **re-registering your Windows server/client** to a vault, ensure that the encryption passphrase provided, matches the passphrase provided during an earlier registration of the server/client to the same vault
 
## **Recommended documents**
[Azure Backup FAQs](https://azure.microsoft.com/en-in/documentation/articles/backup-azure-backup-ibiza-faq/)<br>


