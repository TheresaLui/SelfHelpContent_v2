<properties
    pageTitle="Synchronization issue with specific user, group or contact object"
    description="Synchronization issue with specific user, group or contact object"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    ms.author="cychua"
    displayOrder="53"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview, userandgroups_user, userandgroups_group, directory_overview, directory_ad_connect"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-aadconnect-sync-objectsync-singleobjectissue-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Synchronization issue with specific user, group or contact object

## **Recommended Steps**

1. Check for any synchronization error which corresponds to this object. For details on common synchronization errors, refer to article [Troubleshooting Errors during synchronization](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-sync-errors). Synchronization errors are available to customers in the following ways:

    * Identity synchronization error report - this is an email notification that is sent to the Technical Notification contact for the tenant whenever Azure AD Connect completes a synchronization cycle with errors
    * Under the [Synchronization Service Manager Operation tab](https://docs.azure.cn/active-directory/hybrid/how-to-connect-sync-service-manager-ui-operations)

2. Check for duplicate attribute errors under [Duplicate Attributes Resiliency](https://docs.azure.cn/active-directory/hybrid/how-to-connect-syncservice-duplicate-attribute-resiliency) feature
3. If no error is found for this object, follow the troubleshooting steps described in article [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-object-not-syncing)

## **Recommended Documents**

* [Troubleshooting Errors during synchronization](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-sync-errors)
* [Identity synchronization and duplicate attribute resiliency](https://docs.azure.cn/active-directory/hybrid/how-to-connect-syncservice-duplicate-attribute-resiliency)
* [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-object-not-syncing)
