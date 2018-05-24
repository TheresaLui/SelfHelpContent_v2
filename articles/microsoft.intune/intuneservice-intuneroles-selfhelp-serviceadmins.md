<properties
	pageTitle="I added a user to an Intune role but they still have full access to the Intune Admin Console"
	description="I added a user to an Intune role but they still have full access to the Intune Admin Console"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="intuneroles_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# I added a user to an Intune role but they still have full access to the Intune admin console.

## **Recommended steps**

Verify that the user is not assigned to any of the following roles in the Azure portal:

* Global administrator
* Intune service administrator
* SharePoint administrator

Verify that the user is not assigned to the following role in the Intune classic portal:

* Service administrator

Users in these roles have full access to Intune in the Azure portal. To check the role of a user in the Azure portal go to **Intune** > **Users**. To check the role of a user in the classic portal go to **Admin** > **Service Administrators**.
