<properties
	pageTitle="how to change ownership of my subscription"
	description="how to change ownership of my subscription"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32454918"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="public"
	articleId="howtochangeownershipofmysubscription"
/>

# Change ownership of my subscription

## **Recommended Steps**

To manage access to Azure resources, you must have the appropriate administrator role.<br>

* [Add/Change Administrators](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)<br>
* [Manage access using RBAC and Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)<br>

### Change Account Owner

1. Sign in to the [Account Center](https://account.windowsazure.com/Subscriptions) as the [Account Admin](https://ms.portal.azure.com/#)
2. Select the subscription for which you want to transfer billing ownership
3. On the right side of the page, select **Transfer Subscription**

If your current Account Admin has left and you need to take over ownership, please open a support request so we can validate the transfer.<br>

**Subscription Ownership Transfer prerequisites:** <br>

* Approval Email from Source Account Holder and Destination Account Holder confirming they accept this subscription ownership transfer
* The Account and its subscriptions must continue to be "consumed" in the same country
* If you are Azure customer from Australia/New Zealand, you cannot migrate subscription outside of your Region, nor can any Account/Subscription be migrated into your region
* The destination subscription must have a valid payment instrument <br>
* If transferring Subscription Ownership to a different tenant than the original, the new Account Admin will also be the new Service Admin
* We cannot perform Subscription Ownership Transfer if the subscription has charges already in dunning, Delay Write-off, or Write-off on the source account. You need to pay the charges before we perform the Subscription Ownership Transfer.
* There is no loss of data and downtime, however, AAD services will be affected and you will need to move those services on your own. The list of services can be found [here](https://docs.microsoft.com/azure/active-directory/active-directory-apps-index).<br>
* If Subscription has Invoice Mode of Payment as Payment method, you cannot proceed with Subscription Ownership Transfer
* All Subscription admins and Co-admins get changed to the Destination Account Owner, depending upon tenant. If we transfer the subscription to another tenant, the new AA will also become the new SA and the Co-admins will be lost.<br>
* All Subscription admins and Co-admins get changed to the Destination Account Owner, depending upon tenant. If we transfer the subscription to another tenant, the new AA will also become the new SA and the Co-admins will be lost.
* All billing history will be lost for Source Subscription. Please backup the billing invoices and usage history if required.<br>
* If the subscription is transferred with an existing unpaid balance from the current billing cycle, the pending balance will be transferred to the new Subscription owner
* If we are transferring the subscription from one tenant to another tenant (from one organization to another organization) then the Co-admins from the Source Subscription will not be transferred

Learn more:  [Transfer Ownership of Subscription](https://docs.microsoft.com/azure/billing/billing-subscription-transfer) <br>

### Add Administrator 

To add someone as an administrator for an Azure subscription, assign them the Owner role (an RBAC role) at the subscription scope. The Owner role can manage the resources in the subscription that you assigned and doesn't have access privilege to other subscriptions.<br>

1. Visit [Subscriptions in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
2. Select the subscription that you want to give access
3. Select **Add**. If the Add button is missing, you do not have permission to add permissions.
4. Select **Access control (IAM)** in the list
5. In the **Role** box, select **Owner**
6. In the **Assign access to** box, select **Azure AD user, group, or application**
7. In the **Select** box, type the email address of the user you want to add as Owner. Select the user, and then select **Save**
	
### Add or Change Co-Administrator

Only an [Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#owner) can be added as a Co-administrator. Other users with roles such as [Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#contributor) and [Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#reader) cannot be added as Co-administrators.

### Move Resources 

Azure resources can be moved to either another Azure subscription or another resource group under the same subscription. You can use the Azure portal, Azure PowerShell, Azure CLI, or the REST API to [move resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources). <br>

Learn more on how to move Azure resources: [Tutorial: Move Azure resources to another resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-tutorial-move-resources). <br>

Learn more: [Services that can be moved](https://docs.microsoft.com/azure/azure-resource-manager/move-support-resources). <br>
 
_Note:_ If you want to upgrade your Azure subscription (such as switching from free to pay-as-you-go), you need to convert your subscription.<br>

* To upgrade a free trial, see [Upgrade your Free Trial or Microsoft Imagine Azure subscription to Pay-As-You-Go](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription)
* To change a pay-as-you-go account, see [Change your Azure Pay-As-You-Go subscription to a different offer](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)<br>
* If you can't convert the subscription, [create an Azure support request](https://docs.microsoft.com/azure/azure-supportability/how-to-create-azure-support-request). Select Subscription Management for the issue type


## **Recommended Documents**

* [What is role-based access control (RBAC)?](https://docs.microsoft.com/azure/role-based-access-control/overview)
* [Understand the different roles in Azure](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles)
* [Associate or add an Azure subscription to Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory)
* [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)
* [Tutorial: Grant access for a user using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/quickstart-assign-role-user-portal)
* [Troubleshoot RBAC in Azure](https://docs.microsoft.com/azure/role-based-access-control/troubleshooting)
* [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/azure-resource-manager/management-groups-overview)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Manage (Reactivate/cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
