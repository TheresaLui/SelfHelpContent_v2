<properties
    pageTitle="External Collaboration Settings"
    description="External Collaboration Settings"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="marwaIDcxp"
    ms.author="marwa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615396"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="1894f02c-a027-4547-a9fe-fee4840432f5"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# External Collaboration Settings

**Announcement** 
* [Deprecation of WebView sign-in support from Google starting January 4, 2021](https://docs.microsoft.com/azure/active-directory/external-identities/google-federation#deprecation-of-webview-sign-in-support). Test whether your apps are affected by following [Google’s guidance](https://developers.googleblog.com/2020/08/guidance-for-our-effort-to-block-less-secure-browser-and-apps.html) on testing compatibility
* Make sure to use the system webview or the system browser when signing in your users with consumer Google accounts

## **Recommended Steps**

### Manage Invitation Settings 

Confirm that you have [configured the external collaboration settings](https://docs.microsoft.com/azure/active-directory/b2b/delegate-invitations) to allow the appropriate people to send invitations. 
 
### Manage Guest User Access Permissions 

1. Global admins can manage guest access permissions in the directory through the Azure portal by configuring the guest access permissions on the **External Collaboration Settings** page. [Learn more about this setting](https://docs.microsoft.com/azure/active-directory/fundamentals/users-default-permissions). 

2. If you would like your guests to access apps such as Teams or SharePoint, confirm that you've configured those apps to allow guest access. Learn more about the [Teams settings](https://docs.microsoft.com/microsoftteams/guest-access) and [Sharepoint](https://docs.microsoft.com/sharepoint/external-sharing-overview). 


## **Recommended Documents**

### Configuring invitations: 

* [Enable B2B external collaboration and manage who can invite guests](https://docs.microsoft.com/azure/active-directory/b2b/delegate-invitations)
* [Allow or block invitations to users from specific organizations](https://docs.microsoft.com/azure/active-directory/b2b/allow-deny-list)

### Configuring allowed identity providers: 

* [Google Federation](https://docs.microsoft.com/azure/active-directory/b2b/google-federation)
* [Direct Federation](https://docs.microsoft.com/azure/active-directory/b2b/direct-federation) 
* [Email one-time Passcode Authentication](https://docs.microsoft.com/azure/active-directory/b2b/one-time-passcode)

### Other links: 

* [Troubleshooting Azure Active Directory B2B Collaboration](https://docs.microsoft.com/azure/active-directory/b2b/troubleshoot)
* [Azure Active Directory B2B Best Practices](https://docs.microsoft.com/azure/active-directory/b2b/b2b-fundamentals) 
