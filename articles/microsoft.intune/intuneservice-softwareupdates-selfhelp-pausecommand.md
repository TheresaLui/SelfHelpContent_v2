<properties
	pageTitle="My devices installed their scheduled updates, even though I issued a pause command."
	description="My devices installed their scheduled updates, even though I issued a pause command."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="software_updates_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="6374e0bf-6359-4631-b522-dde75208a2e5"
	ownershipId="IntuneCxP_Intune"
/>

# My devices installed their scheduled updates, even though I issued a pause command.

## **Recommended steps**

When a pause command is issued, devices do not process the command until the next time they check in to Intune. Because of this, your devices may have:

* Installed the scheduled updates prior to check-in.
* Been powered off when you issued the pause command. In this case, when the devices were powered on, they may have downloaded and installed the scheduled updates prior to check-in.
