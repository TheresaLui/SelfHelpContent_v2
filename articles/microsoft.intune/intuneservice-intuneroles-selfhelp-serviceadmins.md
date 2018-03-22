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

# I added a user to an Intune role but they still have full access to the Intune admin console

## **Recommended steps**

Verify the user is not a global administrator, Intune service administrator, sharepoint administrator, or service administrator in the Intune silverlight console.  These administrators have full permissions in the Intune azure portal.  You can check if a user is a Intune silverlight portal service administrator by logging into the [Intune classic portal](https://admin.manage.microsoft.com) and navigating to admin, service administrators.


