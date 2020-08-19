<properties
	pageTitle="Set device compliance - Create Windows Policy"
	description="Set device compliance - Create Windows Policy"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599628"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2cd84cab-926d-447a-9ec7-21217c7cf7e5"
	ownershipId="IntuneCxP_Intune"
/>

# Set device compliance - Create Windows Policy

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**My devices show as not compliant, but I didn't assign a compliance policy to them.**

By default, Intune looks at policy deployment and device health to determine if a device is compliant. In some cases, if no policy is assigned, the device may show as not compliant. Use the following steps to help you determine why they appear this way.

* If you've configured conditional access, specify your compliance requirements by deploying a compliance policy to the groups that have been assigned a conditional access policy. 
* If you don't intend to use conditional access and want the devices to report as compliant, regardless if a compliance policy is assigned or not, go to **Device compliance > Compliance policy settings**. Next to **Mark devices with no compliance policy assigned as** select **Compliant**.

**My devices show as not compliant, even though all devices are enrolled and have compliance policies assigned to them.**

* Go to **Device Compliance > Compliance policy settings** and check what's set for the **Compliance Status Validity period**. The default value is 30 days. Devices become non-compliant when they don't report to Intune within the specified period of days.
* Go to **Device Compliance > Compliance policy settings**. If **Enhanced Jailbreak Detection** is enabled, make sure device users have:
  1.	Turned on Location Services.
  2.	Allowed the Company Portal to access their devices' location.  
* Users that are already flagged for noncompliance might need to:
  1.	Exit the Company Portal app.
  2.	Reopen the app.
  3.	Select the noncompliant device > **Check for compliance**. Normally, this check is done during regular device check in. 

**A BitLocker-encrypted Windows 10 device shows as not compliant in Intune.**

The problem occurs when BitLocker encryption isn't finished, and based on factors such as the disk size, number of files, and BitLocker settings. BitLocker encryption might take longer to complete than a scheduled sync. After encryption is complete, the device will update to a compliant status. 

To check the local status of a BitLocker encryption, run the command **manage-bde-status** from an elevated PowerShell window. Encryption is complete when you see "Percentage Encrypted: 100%" for all drives. For more information about BitLocker management, see the article [BitLocker: Management for Enterprises](https://docs.microsoft.com/windows/security/information-protection/bitlocker/bitlocker-management-for-enterprises) in the Windows documentation.

**Users with Windows devices are not being prompted for password compliance.**

Password compliance policies only apply to local accounts. Azure Active Directory (Azure AD) users are subject to Azure AD password requirements and are not evaluated for conditional access.

For local accounts, this behavior is expected. The new password compliance rules will be enforced the next time the user signs out or signs in, or when they press **Ctrl-Alt-Del** and change their password. 

## **Recommended documents**

* [How to create a device compliance policy for Windows devices in Intune](https://docs.microsoft.com/intune/compliance-policy-create-windows)<br>
* [Get started with Intune device compliance policies](https://docs.microsoft.com/intune/device-compliance-get-started)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
