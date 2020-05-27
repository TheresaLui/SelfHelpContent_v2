<properties
    pageTitle="How to change the default directory of a subscription"
    description="How to change the default directory of a subscription"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="Jeffsta-MSFT"
    ms.author="jeffsta"
    displayOrder="16"
    selfHelpType="resource"
    resourceTags="Azure_RBAC"
    cloudEnvironments="MoonCake"
    articleId="activedirectory-rbac-default-directory-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Unable to change the default directory of a subscription

Changing the default directory of a subscription is performed by transferring the subscription to a user who is in the desired directory.

## **Recommended Steps**

1.	Sign in to the [Azure subscription portal](https://account.windowsazure.cn/Subscriptions) with an account that is the Account Administrator of the subscription to transfer subscription ownership.
2.	Ensure that your target user is in the desired directory and that you would like them to be the subscription owner.
3.	Click **Transfer subscription**.
4.	Specify the recipient. The recipient automatically gets an email with an acceptance link.
5.	The recipient clicks the link and follows the instructions, including entering their payment information. When the recipient succeeds, the subscription is transferred. 
7. The default directory of the subscription is changed to the directory that the user is in if the subscription ownership transfer is successful.

## **Recommended Documents**

* [Transfer ownership of an Azure subscription](https://docs.azure.cn/billing/billing-subscription-transfer#frequently-asked-questions-faq)
* [Understanding resource access in Azure](https://docs.azure.cn/role-based-access-control/rbac-and-directory-admin-roles)
* [Add or change Azure Administrator roles that manage subscriptions](https://docs.azure.cn/billing/billing-add-change-azure-subscription-administrator) 
* [Types of Azure admin accounts](https://docs.azure.cn/billing/billing-add-change-azure-subscription-administrator#types-of-azure-admin-accounts)
* [Office 365 admin roles](https://support.office.com/article/About-Office-365-admin-roles-da585eea-f576-4f55-a1e0-87090b6aaa9d)
