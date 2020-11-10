<properties
	pageTitle="Set device compliance - Monitor device compliance"
	description="Set device compliance - Monitor device compliance"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599657"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="816b5054-4ede-4dba-8962-e02c9e5c3ad0"
	ownershipId="IntuneCxP_Intune"
/>

# Set device compliance - Monitor device compliance

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**A BitLocker-encrypted Windows 10 device shows as not compliant in Intune.**

The problem occurs when BitLocker encryption isn't finished, and based on factors such as the disk size, number of files, and BitLocker settings. BitLocker encryption might take longer to complete than a scheduled sync. After encryption is complete, the device will update to a compliant status. 

To check the local status of a BitLocker encryption, run the command **manage-bde-status** from an elevated PowerShell window. Encryption is complete when you see "Percentage Encrypted: 100%" for all drives. For more information about BitLocker management, see the article [BitLocker: Management for Enterprises](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-management-for-enterprises) in the Windows documentation.

**Users with Windows devices are not being prompted for password compliance.**

Password compliance policies only apply to local accounts. Azure Active Directory (Azure AD) users are subject to Azure AD password requirements and are not evaluated for conditional access.

For local accounts, this behavior is expected. The new password compliance rules will be enforced the next time the user signs out or signs in, or when they press **Ctrl-Alt-Del** and change their password. 

**In Intune in the Azure portal > Compliance policies > Device Compliance, I see "iOS device is currently busy" in my list of policies.**

* If the device is locked or in low battery mode during check-in, the iOS mobile device management (MDM) agent might notify you that the device is busy. Tell the device user to unlock the device, open the Company Portal app, and force the device to sync or check in with Intune.

* By default, the device is scheduled to check in at least every 8 hours, but if the iOS MDM agent returns this error, the policy might take a longer time to be enforced on the device. 

* If the user is unavailable, you can force a device sync from the **Azure Portal > Devices > All devices**.  Simply select the affected device **> Sync**. However, the forced sync might be susceptible to the same busy message for the reasons stated above. 

**I don't see my Mac device under Intune in the Azure portal. It is, however, showing under Azure Active Directory.**

Complete the following steps to make sure Jamf is integrated with Intune.

1. Go to the Jamf self-service portal and launch the Company Portal app. For information about how to install and configure Jamf with Intune, see the following articles:

   * [Microsoft Intune and Jamf Pro: Better Together to Manage and Secure Macs](https://cloudblogs.microsoft.com/enterprisemobility/2017/12/14/microsoft-intune-and-jamf-pro-better-together-to-manage-and-secure-macs/)
   * [Integrate Jamf Pro with Intune for compliance](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)

2. Tell the device owner to go to the Jamf self-service portal and re-run the device registration policy.  The Mac OS should now appear under the Intune device list in the Azure portal as well as in Azure AD.

**Something is requiring Android Enterprise devices to be encrypted. However, our organization does not have a policy that enforces encryption on these devices.**

This behavior is expected. Google requires all devices enrolled with Android Enterprise to be encrypted.

**The Android Enterprise devices in my organization are compliant with all of our policies, but they are still showing as not compliant.**

If your devices use Microsoft Intune Exchange On-premises or Exchange Online Dedicated, you must:

  1.	Deploy an email profile for the Gmail or Nine Work for Android Enterprise app.
  2.	Deploy those apps as a required installation.

For more information about configuring policies for devices that use these environments, see the [Intune documentation](https://docs.microsoft.com/intune/device-profile-create).

## **Recommended documents**

* [Monitor Intune Device compliance policies](https://docs.microsoft.com/intune/compliance-policy-monitor)<br>
* [Get started with Intune device compliance policies](https://docs.microsoft.com/intune/device-compliance-get-started)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
