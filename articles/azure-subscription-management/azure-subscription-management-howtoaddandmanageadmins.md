<properties
	pageTitle="how to add and manage admins"
	description="how to add and manage admins"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32454920"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
/>

# how to add and manage admins

## **Recommended steps**

To manage access to Azure resources, you must have the appropriate administrator role.<br>
[Administrator roles - Understand limits & permissions by role and how to update them](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)

**How to Add an RBAC Owner for a subscription in Azure portal ?**<br>
To add someone as an administrator for an Azure subscription, assign them the [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) role (an RBAC role) at the subscription scope. The Owner role can manage the resources in the subscription that you assigned and doesn't have access privilege to other subscriptions.

1. Visit [Subscriptions in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade).
2. Select the subscription that you want to give access.
3. Select **Add**. (If the Add button is missing, you do not have permission to add permissions.)
4. Select **Access control (IAM)** in the list.
5. In the **Role** box, select **Owner**.
6. In the **Assign access to** box, select **Azure AD user, group, or application**.
7. In the **Select** box, type the email address of the user you want to add as Owner. Select the user, and then select **Save**.

**How do  Add or change Co-administrator ?**<br>
Only an [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) can be added as a Co-administrator. Other users with roles such as [Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) and [Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#reader) cannot be added as Co-administrators.

## **Recommended docunents**

* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Manage (Reactivate/cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
* [How to Edit profile](https://docs.microsoft.com/azure/billing/billing-how-to-change-azure-account-profile)
