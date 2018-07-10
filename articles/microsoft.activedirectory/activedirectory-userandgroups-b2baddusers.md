<properties
    pageTitle="User and Group Management/Adding Users (B2B)"
    description="Azure Active Directory case submission self help"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="sasubram"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32565671"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# Adding B2B collaboration guest users

## **Recommended steps**

### **How to add guest users**

Use the **New Guest user** button on the **All users** blade to add guest users. Enter their email address and optional message and select **Invite**.

You can also add new guest users directly to a group by using the "invite" option in the **Add member** experience for groups. You can add existing guest users to the group through the **Add member** experience without using the "invite" option.


You can also add new guest users directly to an application by using the "invite" option in the **Users and Groups @gt; Add user @gt; Users and Groups** experience for groups. You can add existing guest users to the group through the **Users and Groups @gt; Add user @gt; Users and Groups** experience without using the "invite" option.
 
### **Unable to invite user as guest**

Use the **New Guest user** button in the **All users** to add guest users. Just enter their email address and optional message and select **Invite**.

You can also add new guest users directly to a group by using the "invite" option in the **Add member** experience for groups. You can add existing guest users to the group through the **Add member** experience without using the "invite" option.

You can also add new guest users directly to an application by using the "invite" option in the **Users and Groups @gt; Add user @gt; Users and Groups** experience for groups. You can add existing guest users to the group through the **Users and Groups @gt; Add user @gt; Users and Groups** experience without using the "invite" option.

If you are still unable to invite, please create a support ticket and let us know the details of the issue and we will be glad to help.

### **Unable to add an invited guest user to the directory**

Please use the **New Guest user** button in the "All users" to add guest users. Just enter their email address and optional message and select "Invite"

You can also add new guest users directly to a group by using the "invite" option in the **Add member** experience for groups. You can add existing guest users to the group through the **Add member** experience without using the "invite" option.

You can also add new guest users directly to an application by using the "invite" option in the **Users and Groups @gt; Add user @gt; Users and Groups** experience for groups. You can add existing guest users to the group through the **Users and Groups @gt; Add user @gt; Users and Groups** experience without using the "invite" option.

If you are still unable to invite, please create a support ticket and let us know the details of the issue and we will be glad to help.

### **How can a guest leave the directory?**

Currently the only way to do this to contact the other organization's administrator or to create a support ticket for Microsoft.

### **Unable to resend invite to user**

If the guest user has not yet accepted their invitation, navigate to the user's profile and use the **Resend invitation** button. If the user has accepted the invitation already, you will not find this button there - in which case, just email them the link to the app or resource you want them to access.

### **How to add guest users without invitation**

Invitations that are sent by a user in the inviting organization, who is also a member of the invited organization (the organization of the B2B user), do not require redemption by the B2B user. To do this, we recommend that you invite one user from the invited organization to join the inviting organization (yours). Add this user to the guest inviter role in the resource organization. This user can invite other users in the invited organization by using the sign-in UI, PowerShell scripts, or APIs. This way, the B2B user from that organization isn't required to redeem their invitation.

### **Invite does not include personal messages**

To comply with privacy laws, our APIs do not include custom messages in the email invitation when the inviter doesn’t have an email address in the resource organization (otherwise known as the inviting tenancy) or when an app service principal sends the invitation. If this is an important scenario for you, you can suppress our API sending the invitation email and send it through an email mechanism of your choice. Remember to consult your organization’s legal counsel to make sure any email you send this way also complies with privacy laws.

### **Unable to add guest user - getting <DOMAIN> is not a verified domain name in this directory**

Use the **New Guest user** button in the **All users** to add guest users. Just enter their email address and optional message and select **Invite**.

## **Recommended documents**
* [Adding B2B collaboration guests to your Azure AD tenant](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-admin-add-users)
* [B2B collaboration licensing](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-licensing)
* [Troubleshooting B2B collaboration](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-troubleshooting)
* [B2B collaboration frequently asked questions (FAQ)](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-faq)
* [Multi-factor authentication for B2B collaboration users](https://docs.microsoft.com/azure/active-directory/active-directory-b2b-mfa-instructions)

