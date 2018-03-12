<properties
	pageTitle="I added a scope group to a role, but administrators in that role still see other users or devices."
	description="I added a scope group to a role, but administrators in that role still see other users or devices."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="intuneroles_selfhelp"
	productPesIds=""
	cloudEnvironments="public"
/>

# I added a scope group to a role, but administrators in that role still see other users or devices

## **Recommended steps**

Scope groups do not filter out users or devices.  Rather, they limit the Security Groups or users you can assign policy or applications to, or which users can have remote tasks run on their devices.  Assigning policy or applications to a security group that,s not in your Scope Groups will fail.  For more information on Scope groups please review this [documentation](https://docs.microsoft.com/intune/role-based-access-control).


