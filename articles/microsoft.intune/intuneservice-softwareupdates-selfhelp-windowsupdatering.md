<properties
	pageTitle="I configured software updates through a Windows 10 update ring, but the updates are not being deployed."
	description="I configured software updates through a Windows 10 update ring, but the updates are not being deployed."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="software_updates_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# I configured software updates through a Windows 10 update ring, but the updates are not being deployed.

## **Recommended steps**

* Consider changing Windows servicing from a **Semi-Annual Channel** release type to a stricter, more frequent release type such as **Semi-Annual Channel Targeted**

* Check the deferral period for **Quality update** and **Feature update**. The deferral period could lead to delay in updates for up 180 days. 

For more information on these settings see [Manage software updates in Intune.](https://docs.microsoft.com/intune/windows-update-for-business-configure)

