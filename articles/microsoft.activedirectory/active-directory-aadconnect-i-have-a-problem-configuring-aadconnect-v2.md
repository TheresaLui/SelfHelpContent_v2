<properties
    pageTitle="I have a problem configuring AADConnect"
    description="I have a problem configuring AADConnect"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32684508"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="d0286483-22cc-43aa-a225-2e40dd2c110b"
	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>
## **Recommended Steps**

# I have a problem configuring AADConnect

* You have not yet installed Azure AD Connect and want to learn more about it: please read [How to install Azure AD Connect](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-install-express)
* You want to know more about how Azure AD Connect works or what the configuration options are: [Understanding Azure AD Connect sync architecture](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-architecture) or [Understanding the default configuration of Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-default-configuration) might answer your questions
* You have already configured Azure AD Connect and now:

	* [You have a problem configuring attribute filtering](#problem-with-configuring-attribute-filtering)
	* [You have a problem configuring the UPNs (user names) of my users](#problem-with-configuring-UPNs)
	* [You have a problem configuring synchronization cycles](#problem-with-sync-cycle-configuration)

### Problem with configuring attribute filtering

Configuring attribute filtering is an advanced feature. We strongly advise you review the **Recommended Documents** before making any changes to the synchronization rules. Any changes in filtering or scoping may result in the deletion of objects in your target directory.

After reviewing the recommended documents, follow the [instructions in this document to configure attribute filtering](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-configure-filtering#attribute-based-filtering).

### Problem with configuring UPNs

If you want to learn more about how you can configure User Principal Names in Azure AD Connect sync please read [this document](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-userprincipalname).

### Problem with sync cycle configuration

If you have questions about how to configure the Azure AD Connect sync cycle, [this document](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-feature-scheduler) explains how the sync cycle works and how to configure it.

## **Recommended Documents**

* [Azure AD Connect sync: Technical Concepts](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-technical-concepts)
* [Azure AD Connect sync: Understanding the architecture](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-architecture)
* [Azure AD Connect sync: Understanding Declarative Provisioning](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-declarative-provisioning)
* [Azure AD Connect sync: Understanding Declarative Provisioning Expressions](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-declarative-provisioning-expressions)
* [Azure AD Connect sync: Understanding the default configuration](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-default-configuration)
* [Azure AD Connect sync: Understanding Users, Groups, and Contacts](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-user-and-contacts)
* [Azure AD Connect sync: Shadow attributes](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-shadow-attributes)
