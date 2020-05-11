<properties
	pageTitle="Azure Recovery Services Agent installation or registration issues"
	description="Azure Recovery Services Agent installation or registration issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="saurabhsensharma"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32553287"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
	articleId="922bb97a-5ed2-44af-a953-bec1213aed57"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Recovery Services Agent installation or registration issues

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
    3. *.windowsazure.cn
    4. *.partner.microsoftonline.cn
    5. *.chinacloudapi.cn

* Ensure that the **system clock** on the server/client where you install Azure Recovery Services Agent has the correct time for the time zone that the server/client is configured for

* Ensure that .tmp files at **C:\Windows\Temp** directory have been cleaned up before registration

* If you are **re-registering your Windows server/client** to a vault, ensure that the encryption passphrase provided, matches the passphrase provided during an earlier registration of the server/client to the same vault

## **Recommended documents**
[Azure Backup FAQs](https://docs.azure.cn/backup/backup-azure-backup-faq)<br>


