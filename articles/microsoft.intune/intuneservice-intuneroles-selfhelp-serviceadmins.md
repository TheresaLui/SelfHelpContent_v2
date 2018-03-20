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

Verify the user is not a Global Administrator, Intune Service Administrator, SharePoint Administrator, or Service Administrator in the Intune Silverlight console.  These administrators have full permissions in the Intune Azure Portal.  You can check if a user is a Intune Silverlight Portal Service Administrator by logging into the [Intune Classic Portal](https://admin.manage.microsoft.com) and navigating to Admin, Service Administrators.


