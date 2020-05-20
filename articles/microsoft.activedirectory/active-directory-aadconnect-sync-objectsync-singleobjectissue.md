<properties
    pageTitle="Synchronization issue with specific user, group or contact object"
    description="Synchronization issue with specific user, group or contact object"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="221"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview, userandgroups_user, userandgroups_group, directory_overview, directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="506a1887-4b13-48ed-a0f6-be029d7b5e72"
	ownershipId="AzureIdentity_User"
/>

# Synchronization issue with specific user, group or contact object

## **Recommended steps**
1. Check for any synchronization error which corresponds to this object. For details on common synchronization errors, refer to article [Troubleshooting Errors during synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sync-errors). Synchronization errors are available to customers in the following ways:

    * Identity synchronization error report - this is an email notification that is sent to the Technical Notification contact for the tenant whenever Azure AD Connect completes a synchronization cycle with errors.
    
    * Under the [Synchronization Service Manager Operation tab](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-operations).

    * Under Azure AD Connect Health [object-level sync error report](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync). This is currently available to selected customers only.
    
2. Check for duplicate attribute errors under [Duplicate Attributes Resiliency](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency) feature.

3. If no error is found for this object, follow the troubleshooting steps described in article [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-object-not-syncing).

## **Recommended documents**
* [Troubleshooting Errors during synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sync-errors)  
* [Identity synchronization and duplicate attribute resiliency](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency)  
* [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-object-not-syncing)  


