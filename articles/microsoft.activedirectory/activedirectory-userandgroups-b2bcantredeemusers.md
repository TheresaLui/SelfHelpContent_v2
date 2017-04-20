<properties
    pageTitle="User and Group Management/Adding Users (B2B)"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="sasubram"
    displayOrder="2072"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="userandgroups_overview,userandgroups_user,userandgroups_group"
    productPesIds=""
    cloudEnvironments="public"
    />

# I have invited guest users who can't redeem their invitations
 
## **Recommended steps**
1. First, find out if they received their email. This should not happen very often, but perhaps the invitation email is stuck in their spam folder.
If they tell you they haven’t received their email, you can go to the user’s profile in the directory and try resending the invitation.
2. If the user receive the invitation, but can't accept it, it could be that their organization exists in tenant but the recipient’s account does not. And their organization might have disabled the just-in-time creation of accounts that is needed for redemption to succeed. 

  If this is the case, this is happening because the guest user’s organizational policy is blocking this. Please refer the guest user to contact his organization’s admin with the following link: https://docs.microsoft.com/powershell/msonline/v1/set-msolcompanysettings and set `-AllowEmailVerifiedUsers to true`.
  
  Another way they could solve this issue is by allowing syncing the guest user’s object from their on-premises Active Directory.


## **Recommended documents**
* [Adding B2B collaboration guests to your Azure AD tenant](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-admin-add-users)
* [B2B collaboration licensing](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-licensing)
* [Troubleshooting B2B collaboration](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-troubleshooting)
* [B2B collaboration frequently asked questions (FAQ)](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-faq)
* [Multi-factor authentication for B2B collaboration users](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-mfa-instructions)

