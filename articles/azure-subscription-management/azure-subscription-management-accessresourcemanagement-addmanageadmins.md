<properties
	pageTitle="how to add and manage admins"
	description="how to add and manage admins"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632952"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
	articleId="howtoaddandmanageadmins"
/>

# how to add and manage admins

## **Recommended Steps**

To manage access to Azure resources, you must have the appropriate administrator role.<br>

Learn more on [Add/Change Administrators](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)<br>

Learn more on [Manage access using RBAC and Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)<br>

**Add an RBAC Owner for a subscription in Azure portal**<br>

To add someone as an administrator for an Azure subscription, assign them the [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) role (an RBAC role) at the subscription scope. The Owner role can manage the resources in the subscription that you assigned and doesn't have access privilege to other subscriptions.<br>

  1. Visit [Subscriptions in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade).<br>
  2. Select the subscription that you want to give access.<br>
  3. Select **Add**. (If the Add button is missing, you do not have permission to add permissions)<br>
  4. Select **Access control (IAM)** in the list.<br>
  5. In the **Role** box, select **Owner**.<br>
  6. In the **Assign access to** box, select **Azure AD user, group, or application**.<br>
  7. In the **Select** box, type the email address of the user you want to add as Owner. Select the user, and then select **Save**.<br>
	
**Add or change Co-administrator**<br>

Only an [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) can be added as a Co-administrator.Other users with roles such as [Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) and [Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#reader) cannot be added as Co-administrators.<br>

**Update a profile**<br>

  1. Sign in to the [Azure Account Center](https://account.azure.com/Profile).<br>
  2. Select the Edit details button, and then update the Profile information<br>


## **Recommended Documents**

* [What is role-based access control (RBAC)?](https://docs.microsoft.com/azure/role-based-access-control/overview)
* [Understand the different roles in Azure](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles)
* [How to: Associate or add an Azure subscription to Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory)
* [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)
* [Tutorial: Grant access for a user using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/quickstart-assign-role-user-portal)
* [Troubleshoot RBAC in Azure](https://docs.microsoft.com/azure/role-based-access-control/troubleshooting)
* [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/azure-resource-manager/management-groups-overview)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Manage (Reactivate/Cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
