<properties
    pageTitle="Syncing and custom rules"
    description="Syncing and custom rules"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="darora10"
    ms.author="deepakar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629774"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="8b608391-742e-4627-b9da-772a75bb078c"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Syncing and custom rules

## **Recommended Steps**

Please try to use the default rules created by the **Azure AD Connect** without modifying them. However, if you must modify the default rules for your requirements, then you need to be an advanced user. We strongly advise you to go through the **Recommended documents** below, before making any changes to the synchronization rules. Any changes in scoping filters, link types, disabling, or deleting a rule may result in the deletion of objects in your target directory. 

* Here are the [best practices to create custom synchronization rule](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-best-practices-changing-default-configuration)
* After reviewing the recommended documents, follow the [instructions in this document to change default configuration](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-change-the-configuration)

## **Recommended Documents**

* [Azure AD Connect sync: Technical Concepts](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-technical-concepts)
* [Azure AD Connect sync: Understanding the architecture](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-architecture)
* [Azure AD Connect sync: Understanding Declarative Provisioning](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-declarative-provisioning)
* [Azure AD Connect sync: Understanding Declarative Provisioning Expressions](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-declarative-provisioning-expressions)
* [Azure AD Connect sync: Understanding the default configuration](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-default-configuration)
* [Azure AD Connect sync: Understanding Users, Groups, and Contacts](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-user-and-contacts)
* [Azure AD Connect sync: Shadow attributes](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-shadow-attributes)
