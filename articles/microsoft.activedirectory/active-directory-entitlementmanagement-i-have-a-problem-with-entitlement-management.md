<properties
    pageTitle="I have a problem with Entitlement Management"
    description="I have a problem with Entitlement Management"
    service="microsoft.activedirectory"
    resource="activedirectory"
    authors="rodejo"
    ms.author="rodejo"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32692567"
    resourceTags=""
    productPesIds="16577"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    articleId="ed6816a5-dfd0-454c-a8b1-4b4aec1015a0"
	ownershipId="AzureIdentity_ComplianceAndReporting"
/>
# I have a problem with Entitlement Management

## **Recommended Steps**

### I have a problem with the administration of Entitlement Management

- If you get an access denied message when configuring entitlement management, and you are a Global administrator, ensure that your directory has an Azure AD Premium P2 (or EMS E5) license
- If you get an access denied message when creating or viewing access packages, and you are a member of a Catalog creator group, you must create a catalog prior to creating your first access package

### I have a problem managing resources

Roles for applications are defined by the application itself and are managed in Azure AD. If an application does not have any resource roles, entitlement management assigns users to a Default Access role.Note that the Azure portal may also show service principals for services that cannot be selected as applications. In particular, Exchange Online and SharePoint Online are services, not applications that have resource roles in the directory, so they cannot be included in an access package. Instead, use group-based licensing to establish an appropriate license for a user who needs access to those services.

- For a group to be a resource in an access package, it must be able to be modifiable in Azure AD. Groups that originate in an on-premises Active Directory cannot be assigned as resources because their owner or member attributes cannot be changed in Azure AD. Groups that originate in Exchange Online as Distribution groups cannot be modified in Azure AD either.
- SharePoint Online document libraries and individual documents cannot be added as resources. Instead, create an Azure AD security group, include that group and a site role in the access package, and in SharePoint Online use that group to control access to the document library or document.
- If there are users that have already been assigned to a resource that you want to manage with an access package, be sure that the users are assigned to the access package with an appropriate policy. For example, you might want to include a group in an access package that already has users in the group. If those users in the group require continued access, they must have an appropriate policy for the access packages so that they don't lose their access to the group. You can assign the access package by either asking the users to request the access package containing that resource, or by directly assigning them to the access package. For more information, see Change request and approval settings for an access package.
- When you remove a member of a team, they are removed from the Office 365 Group as well. Removal from the team's chat functionality might be delayed. For more information, see Group membership.
- Ensure your directory is not configured for multi-geo. Entitlement management currently does not support multi-geo locations for SharePoint Online. SharePoint Online sites must be in the default geo-location to be governed with entitlement management. For more information, see Multi-Geo Capabilities in OneDrive and SharePoint Online.

### I have a problem with external users

When an external user wants to request access to an access package, make sure they are using the My Access portal link for the access package. For more information, see Share link to request an access package. If an external user just visits myaccess.microsoft.com and does not use the full My Access portal link, then they will see the access packages available to them in their own organization and not in your organization.

- If an external user is unable to request access to an access package or is unable to access resources, be sure to check your settings for external users
- If a new external user, that has not previously signed in your directory, receives an access package including a SharePoint Online site, their access package will show as not fully delivered until their account is provisioned in SharePoint Online. For more information about sharing settings, see Review your SharePoint Online external sharing settings.

### I have a problem with requests

- When a user wants to request access to an access package, be sure that they are using the My Access portal link for the access package. For more information, see Share link to request an access package.
- If you open the My Access portal with your browser set to in-private or incognito mode, this might conflict with the sign-in behavior. We recommend that you do not use in-private or incognito mode for your browser when you visit the My Access portal.
- When a user who is not yet in your directory signs in to the My Access portal to request an access package, be sure they authenticate using their organizational account. The organizational account can be either an account in the resource directory, or in a directory that is included in one of the policies of the access package. If the user's account is not an organizational account, or the directory where they authenticate is not included in the policy, then the user will not see the access package. For more information, see Request access to an access package.
- If a user is blocked from signing in to the resource directory, they will not be able to request access in the My Access portal. Before the user can request access, you must remove the sign-in block from the user's profile. To remove the sign-in block, in the Azure portal, click Azure Active Directory, click Users, click the user, and then click Profile. Edit the Settings section and change Block sign in to No. For more information, see Add or update a user's profile information using Azure Active Directory. You can also check if the user was blocked due to an Identity Protection policy.
- In the My Access portal, if a user is both a requestor and an approver, they will not see their request for an access package on the Approvals page. This behavior is intentional - a user cannot approve their own request. Ensure that the access package they are requesting has additional approvers configured on the policy. For more information, see Change request and approval settings for an access package.

## **Recommended Documents**

* [Troubleshooting Entitlement Management](https://docs.microsoft.com/azure/active-directory/governance/entitlement-management-troubleshoot)
