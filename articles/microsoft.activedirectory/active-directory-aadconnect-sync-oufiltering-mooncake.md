<properties
    pageTitle="Synchronization issue with OU-based filtering"
    description="Synchronization issue with OU-based filtering"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    ms.author="cychua"
    displayOrder="51"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview, userandgroups_user, userandgroups_group"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-aadconnect-sync-oufiltering-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Synchronization issue with OU-based (Organizational Unit) filtering

## **Recommended Steps**

Important points to consider when configuring OU-based filtering:

* After setting up OU-based filtering, you must do a **Full import**, followed by **Delta synchronization** as detailed in article section [Configure filtering - Apply and verify changes](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-configure-filtering#apply-and-verify-changes).

* New OUs created after OU-based filtering has been configured are synchronized by default. If you do not want new OUs to be synchronized, follow the configuration steps described in article section [Configure filtering - Organizational Unit-based filtering](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-configure-filtering#organizational-unitbased-filtering).

* The **ForeignSecurityPrincipals** container should be selected if you have multiple forests with trusts. This container allows cross-forest security group membership to be resolved.

* If you use **group-based filtering** in conjunction with OU-based filtering, the OU where the group and member objects are located must be included.

* Changing the names of existing OUs may cause OU-based filtering to stop working correctly. If you need to change the names of existing OUs, you must reconfigure OU-based filtering on your Azure AD Connect server.

## **Recommended Documents**

* [Azure AD Connect sync: Configure filtering - Organizational Unit-based filtering](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-configure-filtering#organizational-unitbased-filtering)  
