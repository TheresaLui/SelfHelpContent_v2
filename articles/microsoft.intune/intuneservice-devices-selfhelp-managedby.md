<properties
	pageTitle="What is the difference between the enrollment types that appear in the Managed By column?"
	description="What is the difference between the enrollment types that appear in the Managed By column?"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="devices_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="aa52fa88-250d-4623-9b7b-0c130219d4c0"
	ownershipId="IntuneCxP_Intune"
/>

# What is the difference between the enrollment types that appear in the Managed By column?

## **Recommended steps**

* **EAS**: Your devices are managed by Exchange ActiveSync. EAS device records are synced from either the Exchange on-premises connector, or the Exchange Online S2S connector.
* **MDM**: Your devices are managed by Intune. MDM device records sync details about devices enrolled in Intune.
* **EAS/MDM**: If Intune can determine that the EAS and MDM record are the same physical device, it will merge the records. 
* **Jamf**: Your devices are managed by the Jamf Pro service that you integrated with Intune. Device records sync details about the MacOS devices enrolled in Intune.
* **MDM/ConfigMgr Agent**: Your devices are comanaged by Intune MDM and the System Center Configuration Manager. Device records sync devices enrolled in both Intune and Configuration Manager.
* **EAS/MDM/ConfigMgr Agent**: Your devices are comanaged by Intune MDM and the Configuration Manager, and connected to EAS. Device records sync details about devices in Intune, Configuration manager, and either the Exchange on-premises connector, or the Exchange Online S2S connector.
