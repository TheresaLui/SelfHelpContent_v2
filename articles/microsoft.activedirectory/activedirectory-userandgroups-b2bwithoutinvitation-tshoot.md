<properties
    pageTitle="B2B collaboration: I want to add guest users without an invitation"
    description="Azure Active Directory self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="sasubram"
    displayOrder="792"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user,userandgroups_group"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    	articleId="68d45e6c-8e68-46ad-bf5e-d4f455917544"
	ownershipId="AzureIdentity_User"
/>

# B2B collaboration: I want to add guest users without an invitation

## **Recommended steps**

Invitations that are sent by a user in the inviting organization, who is also a member of the invited organization (the organization of the B2B user), do not require redemption by the B2B user. To do this, we recommend that you invite one user from the invited organization to join the inviting organization (yours). Add this user to the guest inviter role in the resource organization. This user can invite other users in the invited organization by using the sign-in UI, PowerShell scripts, or APIs. This way, the B2B user from that organization isn't required to redeem their invitation.

 
## **Recommended documents**
* [Adding B2B collaboration guests to your Azure AD tenant](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-admin-add-users)
* [B2B collaboration licensing](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-licensing)
* [Troubleshooting B2B collaboration](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-troubleshooting)
