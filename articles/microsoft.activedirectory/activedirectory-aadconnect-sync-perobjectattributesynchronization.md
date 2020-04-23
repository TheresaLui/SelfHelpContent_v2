<properties
    pageTitle="Synchronizing AD to Azure AD/Per object or attribute synchronization"
    description="Synchronizing AD to Azure AD/Per object or attribute synchronization"  service="microsoft.activedirectory"
    resource="activedirectory"
    authors="cychua"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32570976"
    resourceTags=""
    productPesIds="14785,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="bd143943-d7e5-4dba-b5e0-f52fae4358cd"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Synchronizing AD to Azure AD/Per object or attribute synchronization

## **Recommended steps**

**Issue with synchronizing specific user, group or contact object**

If you have issues with synchronizing specific object:

  * Check for any synchronization error which corresponds to this object. For details on common synchronization errors, refer to article [Troubleshooting Errors during synchronization](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-troubleshoot-sync-errors). Synchronization errors are available to customers in the following ways:
    * Under Azure AD Connect Health [object-level sync error report](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-sync). This is currently available to selected customers only.
    * Identity synchronization error report - this is an email notification that is sent to the Technical Notification contact for the tenant whenever Azure AD Connect completes a synchronization cycle with errors.
    * Under the [Synchronization Service Manager Operation tab](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-operations).
  * Check for duplicate attribute errors under [Duplicate Attributes Resiliency](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsyncservice-duplicate-attribute-resiliency) feature.

  * If no error is found for this object, follow the troubleshooting steps described in article [Troubleshoot an object that is not synchronizing to Azure AD](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-object-not-syncing).

**Synchronization issue with OU-based (Organizational Unit) filtering**

Important points to consider when configuring OU-based filtering:

  * After setting up OU-based filtering, you must do a **Full import**, followed by **Delta synchronization** as detailed in article section [Configure filtering - Apply and verify changes](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#apply-and-verify-changes).

  * New OUs created after OU-based filtering has been configured are synchronized by default. If you do not want new OUs to be synchronized, follow the configuration steps described in article section [Configure filtering - Organizational Unit-based filtering](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-configure-filtering#organizational-unitbased-filtering).

  * The **ForeignSecurityPrincipals** container should be selected if you have multiple forests with trusts. This container allows cross-forest security group membership to be resolved.

  * If you use **group-based filtering** in conjunction with OU-based filtering, the OU where the group and member objects are located must be included.

  * Renaming existing OUs may cause OU-based filtering to stop working correctly. If you need to change the names of existing OUs, you must reconfigure OU-based filtering on your Azure AD Connect server.
