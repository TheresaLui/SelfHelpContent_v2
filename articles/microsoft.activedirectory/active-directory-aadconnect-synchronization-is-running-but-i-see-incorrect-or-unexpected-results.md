<properties
    articleid="4efbde14-e9a3-4b89-9979-45ff8bf404a5"
    pageTitle="Synchronization is running but I see incorrect or unexpected results"
    description="Synchronization is running but I see incorrect or unexpected results"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32684522"
    resourceTags=""
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Synchronization is running but I see incorrect or unexpected results

## **Recommended Steps**

Please review one of the below options to troubleshoot Azure AD Connect sync if you are seeing incorrect or unexpected results. 

**Note**: **If your Azure AD Connect sync service is not running at all**, please go back to the previous page and select the support sub-topic "*Synchronization does not work at all*". The below common solutions are for those problems where the synchronization service is running but you are seeing incorrect or unexpected results.

 * [I have a problem where **some objects are not syncing**](i-have-a-problem-where-some-objects-are-not-syncing)
 * [I am seeing **unexpected deletes of objects**](i-am-seeing-unexpected-deletes-of-objects)
 * [I am not seeing **expected deletions of objects**](i-am-not-seeing-expected-deletions-of-objects)
 * [I am seeing **duplicate attribute errors**](i-am-seeing-duplicate-attribute-errors)
 * [I have a problem where objects are syncing but there is **an issue with some attribute values**](i-have-a-problem-where-objects-are-syncing-but-there-is-an-issue-with-some-attribute-values)
 * [I am seeing **export errors**](i-am-seeing-export-errors)
### I have a problem where some objects are not syncing

* If an object is not syncing or has a **UPN mismatch**, use the [Azure AD Connect troubleshooting steps](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-objectsync) to investigate and resolve the issue
* If the above steps did not resolve your sync issue, please read [troubleshooting an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-object-not-syncing) 

### I have a problem where objects are syncing but there is an issue with some attribute values

* If you noticed that the **userPrincipalName** or **proxyAddress** is not syncing, it could be because these are [shadow attributes](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-shadow-attributes)
* If the above steps did not resolve your sync issue, try [troubleshooting an attribute not synchronizing to the Azure AD](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-attribute-not-syncing) 

### I am seeing export errors

If you have encountered the synchronization errors in the export, then use the steps outlined in the document below.

* [Troubleshoot export errors during synchronization](https://docs.microsoft.com/azure/active-directory/hybrid/tshoot-connect-sync-errors)

### I am seeing unexpected deletes of objects
The following changes can trigger deletion of objects, one of which may have caused an unexpected deletion:

* Changes to filtering where an entire OU or domain is unselected
* All objects in an OU are deleted
* An OU is renamed so all objects in it are now out of scope for synchronization
* Changing the **Scoping filter** of a synchronization rule
* Disabling a synchronization rule which has **Link Type** property value set to provision
* Changing **Link Type** property value of a synchronization rule from provision to join

Follow this link to [review the objects to be deleted](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-feature-prevent-accidental-deletes).

### I am not seeing expected deletions of objects
This issue might be caused by the **deletion threshold**. When installing Azure AD Connect, prevent accidental deletes is enabled by default and configured to **not allow an export with more than 500 deletes**. This feature is designed to protect you from accidental configuration changes and changes to your on-premises directory that would affect many users and other objects.

To learn more about this feature, how to manage the setting or how to temporarily disable this feature, please [read this document](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-feature-prevent-accidental-deletes).

### I am seeing duplicate attribute errors
If you have encountered the synchronization errors like **QuarantinedAttributeValueMustBeUnique** or **AttributeValueMustBeUnique**, please use the steps outlined in [this document](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-health-diagnose-sync-errors).

## **Recommended Documents**

* [Azure AD Connect sync: Technical Concepts](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-sync-technical-concepts)
* [Azure AD Connect sync: Understanding the architecture](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-architecture)
* [Azure AD Connect sync: Understanding Declarative Provisioning](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-declarative-provisioning)
* [Azure AD Connect sync: Understanding Declarative Provisioning Expressions](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-declarative-provisioning-expressions)
* [Azure AD Connect sync: Understanding the default configuration](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-default-configuration)
* [Azure AD Connect sync: Understanding Users, Groups, and Contacts](https://docs.microsoft.com/azure/active-directory/hybrid/concept-azure-ad-connect-sync-user-and-contacts)
* [Azure AD Connect sync: Shadow attributes](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-shadow-attributes)
