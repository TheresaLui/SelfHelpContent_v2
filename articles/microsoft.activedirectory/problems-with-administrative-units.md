<properties
	pageTitle="Problems with Administrative Units"
	description="Problems with Administrative Units"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="marwaIDCxP"
  	ms.author="marwa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32736805"
	resourceTags=""
	productPesIds="16578"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="2c68dc49-52e0-4142-9e3c-dd84fdbaf79e"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problems with Administrative Units

## **Recommended Steps**

1. Ensure that the user creating the administrative units and assigning roles is a global administrator or a privilege role administrator
2. Make sure you are assigning users directly to the administrative units. Assigning a group to an administrative unit does not assign all the members of the group to the administrative unit.
3. For a bulk operation performed on an administrative unit, the changes may take time to reflect in the UI depending on various factors such as current service load etc

## **Recommended Documents**

* [Get to know about administrative units and supported scenarios](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-administrative-units)
* [Add and manage users in AU](https://docs.microsoft.com/azure/active-directory/users-groups-roles/roles-admin-units-add-manage-users)
* [Assign roles over administrative units as a scope](https://docs.microsoft.com/azure/active-directory/users-groups-roles/roles-admin-units-assign-roles)

### **Troubleshooting and FAQs**

* [Troubleshooting and FAQs](https://docs.microsoft.com/azure/active-directory/users-groups-roles/roles-admin-units-faq-troubleshoot)
