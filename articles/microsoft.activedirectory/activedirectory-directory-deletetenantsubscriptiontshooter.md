<properties 
    pageTitle="I have Microsoft Online Services blocking deletion of my Azure AD"
    description="I have Microsoft Online Services blocking deletion of my Azure AD"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="piotrci"
    displayOrder="1870"
    supportTopicIds="32565594"
    selfHelpType="resource"
    resourceTags="directory_delete"
    productPesIds="14785,16578" 
    cloudEnvironments="public"
 	articleId="72fb9b5a-7925-4358-8f2e-2f62b53755d3"
/>

# I have Microsoft Online Services blocking deletion of my Azure AD

## **Recommended steps**

Organizational subscriptions are related to products that require user-level license assignment, for example: Office 365 Enterprise E3, Enterprise Mobility + Security, or Azure AD Premium. To delete an Azure AD tenant, all subscriptions associated to the tenant need to be in a completely **Deprovisioned** state. Deprovisioning occurs after one or more of the following occurs:

* A canceled subscription in the Admin Center is deleted no later than 180 days after cancellation, and marked as **Deprovisioned**
* You transfer subscriptions to another tenant
* You create a support request for immediate cancellation of your subscription. Learn more about [Subscription Lifecycle management and retention](https://support.office.com/article/What-happens-to-my-data-and-access-when-my-Office-365-for-business-subscription-ends-4436582f-211a-45ec-b72e-33647f97d8a3).

To view the list of all subscriptions present in your tenant, go to the [Office 365 Admin Center-&gt;Billing-&gt;Subscriptions](https://portal.office.com/adminportal/home#/subscriptions). You view each type of subscription offer (for example, trial or paid) as well as their state (active or expiring).

Your ability to manage subscriptions depends on how they were originally purchased:

1. Paid or trial seat-based subscriptions like Office 365 Enterprise E3, EMS or Azure AD Premium can be managed via the Office 365 Admin portal. If you wish to cancel a subscription you can do so by the following: Navigate to the Admin portal, go to the **Subscriptions** page and find the subscription you wish to manage in the list, then select **Cancel**. Then select **Confirm Cancellation**. If you wish to expedite your subscription to immediate cancel *before* its natural subscription lifecycle to delete an Azure AD tenant you will need to escalate through Support. Learn more about [Azure billing or Office 365 Business support](https://support.office.com/article/Contact-Office-365-for-business-support-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b).

2. Purchases made with an Enterprise Agreement (EA) cannot be canceled in the Admin Center. Please contact your Account Manager to manage EA subscriptions. Learn more about [Enterprise Agreement enrollment](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer#can-i-migrate-from-pay-as-you-go-to-cloud-solution-provider)

3. Subscriptions created by a Cloud Solution Provider (CSP) partner cannot be canceled in the Admin Center. Please contact the partner using the information provided in the Admin Center for that subscription.

If you would like to move an Azure subscription to a different Azure AD tenant or Office 365, you can move your Pay-As-You-Go, Visual Studio, Action Pack or BizSpark subscription in the Account Center via self-service transfer. Learn more on [How to transfer ownership of an Azure subscription](https://docs.microsoft.com/azure/billing/billing-subscription-transfer).

## **Recommended documents**

* [How Azure subscriptions are associated with Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory)

* [Deleting Users from Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-users-delete-user-azure-portal)

* [Removing applications in the directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#removing-an-application)

* [Transfer ownership of an Azure subscription to another account](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)

* [Additional information on deleting an Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-administer#how-can-i-delete-an-azure-ad-directory)
