<properties 
    pageTitle="I have Microsoft Online Services blocking deletion of my Azure AD"
    description="I have Microsoft Online Services blocking deletion of my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    ms.author="piotrci"
    displayOrder="42"
    supportTopicIds="32565595, 32565596"
    selfHelpType="resource"
    resourceTags="directory_delete"
    productPesIds="16578" 
    cloudEnvironments="MoonCake"
 	articleId="activedirectory-directory-deletetenantsubscriptiontshooter-mooncake"
	ownershipId="AzureIdentity_User"
/>

# I have Microsoft Online Services blocking deletion of my Azure AD

## **Recommended Steps**

Organizational subscriptions are related to products that require user-level license assignment, for example: Office 365 Enterprise E3, Enterprise Mobility + Security, or Azure AD Premium. To delete an Azure AD tenant, all subscriptions associated to the tenant need to be in a completely **Deprovisioned** state. Deprovisioning occurs after one or more of the following occurs:

* A canceled subscription in the Admin Center is deleted no later than 180 days after cancellation, and marked as **Deprovisioned**
* You transfer subscriptions to another tenant. For guidance on adding an existing subscription to an Azure AD tenant, see [Associate or add an Azure subscription to your Azure Active Directory tenant](https://docs.azure.cn/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory).
* You create a support request for immediate cancellation of your subscription. Learn more about [Subscription Lifecycle management and retention](https://support.office.com/article/What-happens-to-my-data-and-access-when-my-Office-365-for-business-subscription-ends-4436582f-211a-45ec-b72e-33647f97d8a3).

To view the list of all subscriptions present in your tenant, go to the [Office 365 Admin Center-&gt;Billing-&gt;Subscriptions](https://portal.office.com/adminportal/home#/subscriptions). You view each type of subscription offer (for example, trial or paid) as well as their state (active or expiring).

Your ability to manage subscriptions depends on how they were originally purchased:

1. Paid or trial seat-based subscriptions like Office 365 Enterprise E3, EMS or Azure AD Premium can be managed via the Office 365 Admin portal. If you wish to cancel a subscription you can do so by the following: Navigate to the Admin portal, go to the **Subscriptions** page and find the subscription you wish to manage in the list, then select **Cancel**. Then select **Confirm Cancellation**. If you wish to expedite your subscription to immediate cancel *before* its natural subscription lifecycle to delete an Azure AD tenant you will need to escalate through Support. Learn more about [Azure billing or Office 365 Business support](https://support.office.com/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).
2. Purchases made with an Enterprise Agreement (EA) cannot be canceled in the Admin Center. Please contact your Account Manager to manage EA subscriptions.
3. Subscriptions created by a Cloud Solution Provider (CSP) partner cannot be canceled in the Admin Center. Please contact the partner using the information provided in the Admin Center for that subscription.

If you would like to move an Azure subscription to a different Azure AD tenant or Office 365, you can move your Pay-As-You-Go, Visual Studio, Action Pack or BizSpark subscription in the Account Center via self-service transfer. Learn more on [How to transfer ownership of an Azure subscription](https://docs.azure.cn/billing/billing-subscription-transfer).

## **Recommended Documents**

* [Deleting Users from Azure Active Directory](https://docs.azure.cn/active-directory/fundamentals/add-users-azure-active-directory)
* [Removing applications in the directory](https://docs.azure.cn/active-directory/develop/quickstart-register-app#removing-an-application)
* [Transfer ownership of an Azure subscription to another account](https://docs.azure.cn/billing/billing-subscription-transfer)
* [Additional information on deleting an Azure AD](https://docs.azure.cn/active-directory/fundamentals/active-directory-whatis#how-can-i-delete-an-azure-ad-directory)
