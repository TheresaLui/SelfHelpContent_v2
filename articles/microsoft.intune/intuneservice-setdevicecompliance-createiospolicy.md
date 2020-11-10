<properties
	pageTitle="Set device compliance - Create iOS Policy"
	description="Set device compliance - Create iOS Policy"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599626"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ffe93766-e81a-44b9-98dc-599b0af4d711"
	ownershipId="IntuneCxP_Intune"
/>

# Set device compliance - Create iOS Policy

## **Recommended Steps**

Depending on your scenario, follow the appropriate troubleshooting steps outlined below. 

**In Intune in the Azure portal > Compliance policies > Device Compliance, I see "iOS device is currently busy" in my list of policies.**

* If the device is locked or in low battery mode during check-in, the iOS mobile device management (MDM) agent might notify you that the device is busy. Tell the device user to unlock the device, open the Company Portal app, and force the device to sync or check in with Intune.

* By default, the device is scheduled to check in at least every 8 hours, but if the iOS MDM agent returns this error, the policy might take a longer time to be enforced on the device. 

* If the user is unavailable, you can force a device sync from the **Azure Portal > Devices > All devices**.  Simply select the affected device **> Sync**. However, the forced sync might be susceptible to the same busy message for the reasons stated above. 

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

* [Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
* [Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
* [How to create a device compliance policy for iOS devices in Intune](https://docs.microsoft.com/intune/compliance-policy-create-ios)<br>
* [Get started with Intune device compliance policies](https://docs.microsoft.com/intune/device-compliance-get-started)<br>
