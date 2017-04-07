<properties 
    pageTitle="Trouble with creating and populating a Dynamic Group"
    description= "Trouble with creating and populating a Dynamic Group "
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="kcontrac"
    displayOrder="2519"
    selfHelpType="resource"
    resourceTags="userandgroups_overview,userandgroups_group"
    cloudEnvironments="public"
 />


# Trouble with creating and populating a Dynamic Group

## **Recommended steps**
1.	While constructing the rule, if you cannot find the built-in User Attributes, ensure that the attribute is in the [list of supported properties] (https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#supported-properties).
2.	While constructing the rule, if you are looking for built-in Device Attributes, ensure that the attribute is in the list of [device attributes](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#using-attributes-to-create-rules-for-device-objects).
3.	While constructing the rule, if the attribute is not found in Simple Rule drop-down, you could also use the Advanced Rule to construct the body of an Advanced Rule. Ensure that the syntax is accurate and that the property type and value match. Also ensure that you have added the appropriate object prefix to select the property; for example, user.country, device.deviceOSType.
Guidelines on how to create an Advanced Rule can be found here: https://docs.microsoft.com/en-us/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#constructing-the-body-of-an-advanced-rule 
4.	While constructing the rule, in addition to the built-in user and device attributes, you could also use [Extension Attributes](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal#extension-attributes-and-custom-attributes). These should be visible in the drop-down list while creating a simple rule. The custom attribute name can be found in the directory by querying a user's attribute using PowerShell and searching for the attribute name. These could also be used when constructing an Advanced Rule.  
5.	Ensure that your tenant has the appropriate license. Dynamic groups require the tenant to have an Azure Active Directory P1 Premium license. The list of Azure Active Directory license plans can be accessed [here](https://www.microsoft.com/cloud-platform/azure-active-directory-pricing). Enterprise Mobility + Security licensing plans can be accessed [here](https://www.microsoft.com/cloud-platform/enterprise-mobility-security-pricing).
6.	Ensure that the Role of the user creating the Dynamic group is a Company Administrator or a User Administrator.  
7.	Please allow time for the group to populate. Depending on the size of your tenant, the group may take up to 24 hours for populating for the first time or after a rule change.

## **Recommended documents**

* [How Azure subscriptions are associated with Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory) 
* [Deleting users from Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)
* [Removing applications in the directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#removing-an-application) 
* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)
* [Additional information on deleting an Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administer#how-can-i-delete-an-azure-ad-directory) 