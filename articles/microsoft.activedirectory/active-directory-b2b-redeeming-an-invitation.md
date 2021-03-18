<properties
    pageTitle="Problem redeeming an invitation"
    description="Problem redeeming an invitation"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="marialai"
    ms.author="marwa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32615429"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="1f52c6d5-cfce-4d14-8b87-c1023bac3bea"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem redeeming an invitation

**Announcement** 
* [Deprecation of WebView sign-in support from Google starting January 4, 2021](https://docs.microsoft.com/azure/active-directory/external-identities/google-federation#deprecation-of-webview-sign-in-support). Test whether your apps are affected by following [Google’s guidance](https://developers.googleblog.com/2020/08/guidance-for-our-effort-to-block-less-secure-browser-and-apps.html) on testing compatibility
* Make sure to use the system webview or the system browser when signing in your users with consumer Google accounts

## **Recommended Steps**

* For a guest user to access resources, the user must first explicitly [consent to participate in your directory](https://docs.microsoft.com/azure/active-directory/b2b/redemption-experience). The user can either accept the invitation that was sent by email or can access a URL that includes the ID of your tenant.
* Resend the invitation to a guest user. To resend the invitation, find the guest user in the [All users](https://portal.azure.com/#blade/Microsoft_AAD_IAM/UsersManagementMenuBlade/AllUsers) blade. Click the user's name to open the user profile, and then click **Resend invitation** in the Identity section.
* If the guest user has an email address that is shared by both a Microsoft account and an Azure AD account, make sure that the user accesses resources using the account context in which the user accepted the invitation. For new invitations to users with a Microsoft account and an Azure AD account that share an email address, the new B2B invitation is always accepted in the context of the Azure AD account.

## **Recommended Documents**

* [Issues with signing in to application(s) **using Chrome browser only**](https://docs.microsoft.com/office365/troubleshoot/miscellaneous/chrome-behavior-affects-applications)
* [Redeeming a B2B invitation](https://docs.microsoft.com/azure/active-directory/b2b/redemption-experience)<br>
* [Azure AD B2B documentation](https://docs.microsoft.com/azure/active-directory/b2b/)
