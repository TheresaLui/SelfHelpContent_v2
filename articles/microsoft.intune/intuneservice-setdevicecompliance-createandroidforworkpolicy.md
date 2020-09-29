<properties
	pageTitle="Set device compliance - Create an Android for Work Policy"
	description="Set device compliance - Create an Android for Work Policy"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599624"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="2074c917-8ebe-478b-a161-1e20062cc7b5"
	ownershipId="IntuneCxP_Intune"
/>

# Set device compliance - Create an Android for Work Policy

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**Something is requiring Android Enterprise devices to be encrypted. However, our organization does not have a policy that enforces encryption on these devices.**

This behavior is expected. Google requires all devices enrolled with Android Enterprise to be encrypted.

**The Android Enterprise devices in my organization are compliant with all of our policies, but they are still showing as not compliant.**

If your devices use Microsoft Intune Exchange On-premises or Exchange Online Dedicated, you must:

  1.	Deploy an email profile for the Gmail or Nine Work for Android Enterprise app.
  2.	Deploy those apps as a required installation.

For more information about configuring policies for devices that use these environments, see the [Intune documentation](https://docs.microsoft.com/intune/device-profile-create).

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

* [How to create a device compliance policy for Android for Work devices in Intune](https://docs.microsoft.com/intune/compliance-policy-create-android-for-work)<br>
* [Get started with Intune device compliance policies](https://docs.microsoft.com/intune/device-compliance-get-started)<br>
* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
