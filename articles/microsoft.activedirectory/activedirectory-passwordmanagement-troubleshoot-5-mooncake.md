<properties
    pageTitle="I don't think I have the correct permissions, firewall rules, or connection settings for password writeback"
    description="Top Tips from customers - Tip 6"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="gahug"
    ms.author="gahug"
    displayOrder="19"
    selfHelpType="resource"
    resourceTags="sspr_passwordreset"
    cloudEnvironments="MoonCake"
    articleId="activedirectory-passwordmanagement-troubleshoot-5-mooncake"
	ownershipId="AzureIdentity_User"
/>
# I don't think I have the correct permissions, firewall rules, or connection settings for password writeback

## **Recommended Steps**

In order for writeback to work correctly, you must ensure:

1. The proper **Active Directory permissions** have been set for users using the password writeback feature such that they have rights to modify their own passwords and account unlock flags in AD
2. The proper **firewall ports** have been opened to allow the password writeback service to communicate securely with the outside world using an outbound connection
3. The proper **firewall exceptions** have been made for key password reset service URLs, such as Service Bus
4. Your **proxy and firewall are not killing idle outbound connections**, we recommend 10 minutes or longer
