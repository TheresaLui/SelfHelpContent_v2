<properties
	pageTitle="In Intune in the Azure portal > Compliance policies > Device Compliance, I see iOS device is currently busy in my list of policies."
	description="In Intune in the Azure portal > Compliance policies > Device Compliance, I see iOS device is currently busy in my list of policies."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devicecompliance_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="667160e9-0135-465f-bb20-5fdda5733534"
	ownershipId="IntuneCxP_Intune"
/>

# In Intune in the Azure portal > Compliance policies > Device Compliance, I see "iOS device is currently busy" in my list of policies.

## **Recommended steps**

Review the following options to determine how to troubleshoot the device error.

* If the device is locked or in low battery mode during check-in, the iOS mobile device management (MDM) agent might notify you that the device is busy. Tell the device user to unlock the device, open the Company Portal app, and force the device to sync or check in with Intune.

* By default, the device is scheduled to check in at least every 8 hours, but if the iOS MDM agent returns this error, the policy might take a longer time to be enforced on the device. 

* If the user is unavailable, you can force a device sync from the **Azure Portal > Devices > All devices**.  Simply select the affected device **> Sync**. However, the forced sync might be susceptible to the same busy message for the reasons stated above. 
