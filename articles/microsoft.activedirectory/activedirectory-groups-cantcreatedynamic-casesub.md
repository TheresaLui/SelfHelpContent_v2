<properties
    pageTitle="I can't create and populate a dynamic group"
    description= "Trouble creating and populating a dynamic droup"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="yyuank"
    ms.author="yukarppa"
    displayOrder=""
    supportTopicIds="32570978"
    selfHelpType="generic"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="7f7ae579-3adf-49b1-8c83-64ad1a296d30"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# I can't create and populate a dynamic group

## **Recommended Steps**

1. If you cannot find the built-in User Attributes, ensure that the attribute is in the [list of supported properties](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership#supported-properties)
2. If you are looking for built-in Device Attributes, ensure that the attribute is in the list of [device attributes](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership#rules-for-devices)
3. In addition to the built-in user and device attributes, you could also use [Extension Attributes](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership#extension-properties-and-custom-extension-properties). After syncing extension attributes from on-premises Windows Server AD or from a connected SaaS application, the attributes should be visible in the drop-down list of the Rule builder. The custom attribute name can be found in the directory by querying a user's attribute using PowerShell and searching for the attribute name. These could also be used when constructing rules in the Rule syntax.  
4. Ensure that your tenant has the appropriate license. Dynamic groups require the tenant to have an Azure Active Directory P1 Premium license. The list of Azure Active Directory license plans can be accessed [here](https://www.microsoft.com/cloud-platform/azure-active-directory-pricing). Enterprise Mobility + Security licensing plans can be accessed [here](https://www.microsoft.com/cloud-platform/enterprise-mobility-security-pricing).
5. Ensure that the Role of the user creating the Dynamic group is a Global Administrator, Intune Administrator, Group Administrator, or a User Administrator
6. Please allow time for the group to populate. Depending on the size of your tenant, the group may take up to 24 hours for populating for the first time or after a rule change.

## **Recommended Documents**

* [Create attribute-based rules for dynamic group membership](https://docs.microsoft.com/azure/active-directory/active-directory-groups-dynamic-membership-azure-portal)

### **Recommended Videos**
* [Advanced features of group management: group expiration, dynamic groups, and group naming policy](https://www.youtube.com/watch?v=e9zUqQx5upY)
