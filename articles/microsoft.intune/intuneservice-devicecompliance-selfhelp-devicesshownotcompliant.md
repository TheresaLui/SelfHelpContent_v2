<properties
	pageTitle="My devices show as not compliant, but I didn't assign a compliance policy to them."
	description="My devices show as not compliant, but I didn't assign a compliance policy to them."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devicecompliance_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0b2bd6a6-d8a0-4dc2-9ae2-20d28091989f"
	ownershipId="IntuneCxP_Intune"
/>

# My devices show as not compliant, but I didn't assign a compliance policy to them.

## **Recommended steps**

By default, Intune looks at policy deployment and device health to determine if a device is compliant. In some cases, if no policy is assigned, the device may show as not compliant. Use the following steps to help you determine why they appear this way.

* If you've configured conditional access, specify your compliance requirements by deploying a compliance policy to the groups that have been assigned a conditional access policy. 
* If you don't intend to use conditional access and want the devices to report as compliant, regardless if a compliance policy is assigned or not, go to **Device compliance > Compliance policy settings**. Next to **Mark devices with no compliance policy assigned as** select **Compliant**.
