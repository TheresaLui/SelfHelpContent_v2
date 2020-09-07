<properties
    pageTitle="Synchronization issue with specific user, group or contact object"
    description="Synchronization issue with specific user, group or contact object"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32570979"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="1be43fad-d9a2-4a41-b543-2501f79c324f"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Synchronization issue with specific user, group or contact object

## **Recommended steps**

**Issue with synchronizing specific user, group or contact object**

If you have issues with synchronizing specific object:

* Check for any synchronization error which corresponds to this object. For details on common synchronization errors, refer to article [Troubleshooting Errors during synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sync-errors). Synchronization errors are available to customers in the following ways:

  * Under Azure AD Connect Health [object-level sync error report](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync). This is currently available to selected customers only.

  * Identity synchronization error report - this is an email notification that is sent to the Technical Notification contact for the tenant whenever Azure AD Connect completes a synchronization cycle with errors.

  * Under the [Synchronization Service Manager Operation tab](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-operations).

* Check for duplicate attribute errors under [Duplicate Attributes Resiliency](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency) feature.

* If no error is found for this object, follow the troubleshooting steps described in article [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-object-not-syncing).
