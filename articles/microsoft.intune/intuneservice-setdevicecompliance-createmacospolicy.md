<properties
	pageTitle="Set device compliance - Create macOS Policy"
	description="Set device compliance - Create macOS Policy"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599627"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d8ccae4d-fff9-418d-8563-29e5a8969a4d"
	ownershipId="IntuneCxP_Intune"
/>

# Set device compliance - Create macOS Policy

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**I don't see my Mac device under Intune in the Azure portal. It is, however, showing under Azure Active Directory.**

Complete the following steps to make sure Jamf is integrated with Intune.

1. Go to the Jamf self-service portal and launch the Company Portal app. For information about how to install and configure Jamf with Intune, see the following articles:

   * [Microsoft Intune and Jamf Pro: Better Together to Manage and Secure Macs](https://cloudblogs.microsoft.com/enterprisemobility/2017/12/14/microsoft-intune-and-jamf-pro-better-together-to-manage-and-secure-macs/)
   * [Integrate Jamf Pro with Intune for compliance](https://docs.microsoft.com/intune/conditional-access-integrate-jamf)

2. Tell the device owner to go to the Jamf self-service portal and re-run the device registration policy.  The Mac OS should now appear under the Intune device list in the Azure portal as well as in Azure AD.

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

## **Recommended documents**

* [Create a device compliance policy for macOS devices with Intune](https://docs.microsoft.com/intune/compliance-policy-create-mac-os)<br>
* [Get started with Intune device compliance policies](https://docs.microsoft.com/intune/device-compliance-get-started)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
