<properties
	pageTitle="My devices show as not compliant, even though all devices are enrolled and have compliance policies assigned to them."
	description="My devices show as not compliant, even though all devices are enrolled and have compliance policies assigned to them."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devicecompliance_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# My devices show as not compliant, even though all devices are enrolled and have compliance policies assigned to them.

## **Recommended steps**

* Go to **Device Compliance > Compliance policy settings** and check what’s set for the **Compliance Status Validity period**. The default value is 30 days. Devices become non-compliant when they don’t report to Intune within the specified period of days.
* Go to **Device Compliance > Compliance policy settings**. If **Enhanced Jailbreak Detection** is enabled, make sure device users have:
  1.	Turned on Location Services.
  2.	Allowed the Company Portal to access their devices’ location.  
* Users that are already flagged for noncompliance might need to:
  1.	Exit the Company Portal app.
  2.	Reopen the app.
  3.	Select the noncompliant device > **Check for compliance**. Normally, this check is done during regular device check in. 
