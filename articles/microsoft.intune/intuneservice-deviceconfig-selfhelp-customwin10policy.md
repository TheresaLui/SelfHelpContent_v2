<properties
	pageTitle="I'm creating and applying custom Windows 10 policies, but they're not working."
	description="I'm creating and applying custom Windows 10 policies, but they're not working."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="deviceconfiguration_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="0263873e-f96b-47d6-84ef-e101cf169b2f"
	ownershipId="IntuneCxP_Intune"
/>

# I'm creating and applying custom Windows 10 policies, but they're not working.

## **Recommended steps**

Windows 10 OMA-URI settings need to be entered exactly as the Windows CSP expects, meaning that:

* URI strings are case sensitive
* Data type is entered
* Setting value is entered as expected by the OS

Intune does not support every OMA-URI available. For more information about Custom OMA-URI settings, see the [Intune documentation](https://docs.microsoft.com/intune/custom-settings-windows-10). 
