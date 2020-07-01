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
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="howtochangeownershipofmysubscription"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Change ownership of my subscription

## **Recommended Steps**

* [Supported subscription types](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#supported-subscription-types)

### **Transfer billing ownership**

* Sign in to the [Azure portal](https://ms.portal.azure.com/#home) as the [Account Admin](https://ms.portal.azure.com/#) of the billing account that has the subscription you want to transfer
* Search on **Cost Management + Billing**. Select **Subscriptions** from left-pane. Depending on the access, you may need to select a billing scope and then **Subscriptions** or **Azure subscriptions**.
* Select Transfer billing ownership for the subscription you want to transfer
* Enter the email address of a user who's a billing administrator of the account that will be the new owner for the subscription and then select **send transfer request**
* The user gets an email with instructions to review your transfer request. To approve the transfer request, the user selects the link in the email and follows the instructions.

**Note**: If you transfer billing ownership of your subscription to a user's account in another Azure AD tenant, all [role-based access control (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview) assignments to manage resources in the subscription are permanently removed. Only the new owner will have access to manage resources in the subscription. For more information, see [Transferring subscription to a user in another Azure AD tenant](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/known-issues).

If your current Account Admin has left and you need to take over ownership, please open a support request so we can validate the transfer. Learn more: [Transfer Ownership of Subscription](https://docs.microsoft.com/azure/billing/billing-subscription-transfer)

### **Subscription Ownership Transfer prerequisites**

* Transferring a subscription to an account in the same Azure Active Directory tenant have no impact to the resources running in the subscription. However, if subscription is transferred to an account in another tenant, all users, groups, and service principals who had [role based access (RBAC)](https://docs.microsoft.com/azure/role-based-access-control/overview) to manage resources in the subscription lose their access. For more information about adding an exisiting subscription to a tenant, see [Associate or add an Azure subscription to Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-how-subscriptions-associated-directory).
* Subscription Transfer with an existing outstanding amount from the current billing cycle will not be transferred to the new payment instrument in the new account. The only information available to the users in new account is the last month's cost for your subscription. The rest of the usage and billing history does not transfer with the subscription.
* Transfer billing ownership of Enterprise Agreement (EA) subscriptions is currently supported in the Enterprise Agreement Portal only
* Transferring a credit-oriented subscription like Visual Studio, BizSpark, Microsoft Partner Network to a new user requires to have a Visual Studio/Microsoft partner network license to accept the transfer request
* All resources like Virtual Machines, disks, and websites transfer to the new account successfully. The following resources could be affected in a cross-tenant subscription transfer:

**Azure AD Domain Services**

* [Azure Key Vaults](https://docs.microsoft.com/azure/key-vault/key-vault-subscription-move-fix)
* [SQL related users and databases](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure) could be impacted, especially if the customer uses an Azure Active Directory related authentication
* **App Services** configured with Azure Active Directory authentication could be impacted
* **Visual Studio Team** Services accounts connected to Azure subscriptions may temporarily lose access when the connected Azure subscription is cancelled

### **Add/Change Azure subscription administrators**

To add someone as an administrator for an Azure subscription, assign them the Owner role (an RBAC role) at the subscription scope. The Owner role can manage the resources in the subscription that you assigned and doesn't have access privilege to other subscriptions.

1. Visit [subscriptions in Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade). Select the subscription that you want to give access. Select **Add**. If the Add button is missing, you do not have permission to add permissions.
2. Select **Access control (IAM)**in the list. In the **Role** box, select **Owner**. In the **Assign access to** box, select **Azure AD user, group, or application**.
3. In the **Select** box, type the email address of the user you want to add as Owner. Select the user, and then select **Save**.

Learn more: [Change Azure subscription administrator](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)

### **Move Resources**

Azure resources can be moved to either another Azure subscription or another resource group under the same subscription. You can use the Azure portal, Azure PowerShell, Azure CLI, or the REST API to move resources. Moving a resource only moves it to a new resource group or subscription. It doesn't change the location of the resource. 

Learn more:

* [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
* [Checklist before moving resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources)
* [Tutorial: Move Azure resources to another resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-tutorial-move-resources)
* [Services that can be moved](https://docs.microsoft.com/azure/azure-resource-manager/move-support-resources)

**Note**: If you want to upgrade your Azure subscription (such as switching from free to pay-as-you-go), you need to convert your subscription:

  * To upgrade a free trial: [Upgrade your Azure subscription](https://docs.microsoft.com/azure/billing/billing-upgrade-azure-subscription)
  * To change a pay-as-you-go subscription: [Switch subscription offer](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)

## **Recommended Documents**

* [Steps after accepting billing ownership](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#next-steps-after-accepting-billing-ownership)
* Retain billing ownership but change the type of your subscription refer: [Switch your Azure subscription to another offer](https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer)
* Control who can manage resources in a subscription: [Built-in roles for Azure resources](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles)
* [Transferring Visual Studio, Microsoft Partner Network (MPN) and Pay as you go Dev/Test subscriptions](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#transferring-visual-studio-microsoft-partner-network-mpn-and-pay-as-you-go-devtest-subscriptions)
* [Transfer billing ownership of Enterprise Agreement (EA) subscriptions](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#transfer-billing-ownership-of-enterprise-agreement-ea-subscriptions)
* [Transfer Ownership FAQ](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#frequently-asked-questions-faq-for-senders)
* [Troubleshoot Transfer ownership issues](https://docs.microsoft.com/azure/billing/billing-subscription-transfer#troubleshooting)
* [What is role-based access control (RBAC)?](https://docs.microsoft.com/azure/role-based-access-control/overview)
* [Understand the different roles in Azure](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles)
* [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)
* [Tutorial: Grant access for a user using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/quickstart-assign-role-user-portal)
* [Troubleshoot RBAC in Azure](https://docs.microsoft.com/azure/role-based-access-control/troubleshooting)
* [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/azure-resource-manager/management-groups-overview)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Manage (Reactivate/cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
