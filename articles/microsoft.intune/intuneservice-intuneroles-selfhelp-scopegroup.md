<properties
	pageTitle="I added a scope group to a role, but users in that role still see other users or devices."
	description="I added a scope group to a role, but users in that role still see other users or devices."
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="intuneroles_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c7dd7f17-69ff-4283-9412-e326066e123e"
	ownershipId="IntuneCxP_Intune"
/>

# I added a scope group to a role, but users in that role still see other users or devices.

## **Recommended steps**

Scope groups do not filter out users or devices.  Rather scope groups:

* Limit who users can assign policies or applications to
* Allow only specific users to run remote tasks on devices

If a security group is not within your scope group, you will not be able to assign polices or applications to the group. For more information about scope groups see the [Intune documentation.](https://docs.microsoft.com/intune/role-based-access-control)


