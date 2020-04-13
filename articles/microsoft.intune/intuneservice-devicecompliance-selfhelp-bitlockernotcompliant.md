<properties
	pageTitle="A BitLocker-encrypted Windows 10 device shows as not compliant in Intune."
	description="A BitLocker-encrypted Windows 10 device shows as not compliant in Intune."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devicecompliance_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="de0945af-6602-488e-8972-c13d588a3264"
	ownershipId="IntuneCxP_Intune"
/>

# A BitLocker-encrypted Windows 10 device shows as not compliant in Intune.

## **Recommended steps**

The problem occurs when BitLocker encryption isn't finished, and based on factors such as the disk size, number of files, and BitLocker settings. BitLocker encryption might take longer to complete than a scheduled sync. After encryption is complete, the device will update to a compliant status. 

To check the local status of a BitLocker encryption, run the command **manage-bde-status** from an elevated PowerShell window. Encryption is complete when you see "Percentage Encrypted: 100%" for all drives. For more information about BitLocker management, see the article [BitLocker: Management for Enterprises](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-management-for-enterprises) in the Windows documentation.

