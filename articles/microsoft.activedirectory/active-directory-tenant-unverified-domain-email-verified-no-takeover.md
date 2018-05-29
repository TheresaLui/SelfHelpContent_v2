<properties
	pageTitle="Email Verified No Takeover Customer Ready Content"
	description="Domain is verified in an email-verified directory"
	infoBubbleText="See details on the right"
	service="microsoft.activedirectory"
	resource=""
	authors="bernawy"
	displayOrder="2"
	articleId="Tenant_Unverified_Domain_Email_Verified_No_Takeover"
	diagnosticScenario="EmailVerifiedNoTakeover"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Domain is verified in an email-verified directory

We've found that your domain name <!--$domain-->[domain]<!--/$domain--> is verified in another email verified directory <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant-->. A domain name can only be verified in a single directory at a time. The domain name is currently verified in a different directory (using Office 365 or other Azure services), it cannot be verified in your new directory until you perform internal or external force takeover option. When a self-service user signs up for a cloud service that uses Azure AD, they are added to an unmanaged Azure AD directory based on their email domain. For more information about self-service or "viral" signup for a service, see [What is self-service signup for Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-self-service-signup)

**Recommended Steps**

During the process of admin takeover, you can prove ownership as described in [Add a custom domain name to Azure AD](https://docs.microsoft.com/azure/active-directory/add-custom-domain). The next sections explain the admin experience in more detail, but here's a summary:

*	When you perform an ["internal" admin takeover](https://docs.microsoft.com/azure/active-directory/domains-admin-takeover#internal-admin-takeover) of an unmanaged Azure directory, you are added as the global administrator of the unmanaged directory. No users, domains, or service plans are migrated to any other directory you administer.
*	When you perform the Force takeover option as part of ["external admin takeover](https://docs.microsoft.com/azure/active-directory/domains-admin-takeover#external-admin-takeover) of an unmanaged Azure directory, only the domain name will be moved from the email verified directory and added to your existing administered directory. The existing service plan and users will remain on the email verified directory and access to those subscriptions may break if users had UPNs on the <!--$domain-->[domain]<!--/$domain--> domain name. You can run this PowerShell commandlet **_confirm-msoldomain –Domainname <domainname> –ForceTakeover Force_** which will move only the domain name.

Supporting Links: https://docs.microsoft.com/azure/active-directory/domains-admin-takeover

If you would like to delete the domain name from your other tenant <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant--> you can follow the instructions here on how to remove a domain name and its references. If you are not aware of the other directory that has this domain registered, please let us know.

To continue with deleting your domain name in the other tenant <!--$holdingTenant-->[holdingTenant]<!--/$holdingTenant--> proceed with the steps outlined in this article: [Delete a domain name and move it to another Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-domains-manage-azure-portal)