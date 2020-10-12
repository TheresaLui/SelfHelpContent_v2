<properties
	pageTitle="How do I add or manage administrators for my Azure Subscription?"
	description="How do I add or manage administrators for my Azure Subscription?"
	service="azure-subscription-management"
	resource="subscription-management"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632952"
	resourceTags=""
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="accessandresourcemanagementhowtoaddandmanageadmins"
	ownershipId="ASMS_SubscriptionManagement"
/>
 
# How do I add or manage administrators for my Azure Subscription?

## **Recommended Steps**

**Change the Subscription Administrator or Co-administrator**

* The Account Administrator can change both roles whereas the Subscription Administrator can only change Co-administrators in the [Management portal](https://ms.portal.azure.com/): [Add or change Azure subscription administrators](https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator)

**Update the Subscription Administrator or Co-Administrator for Internal (AIRS) Subscriptions**
The Service Administrator or the Co-administrator can self-serve this action by using the steps below:

* Log into the [Azure Portal](https://ms.portal.azure.com/#@microsoft.onmicrosoft.com/dashboard/private/a84d2c8e-8fab-45bd-afa5-7151a29b800f) and click on **Cost Management + Billing** in the left blade
* Click on the line item with your subscription. This will open the Overview for your subscription.
* On the **Subscription** blade, click on **Properties**. Click the **Service Admin** button.
* Enter the email of the user that you want to set as a Service Administrator and click **OK**

**Add/Change/Remove Co-administrator**

* Sign in to the [Azure Portal](https://portal.azure.com/) as a Service Administrator
* Open [Subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) and select a subscription. (Co-admins can only be assigned at the subscription scope)
* Click **Access control (IAM)** and click the **Classic administrators** tab. Now click **Add > Add co-administrator** to open the Add co-admin pane (If the Add co-administrator option is disabled, you do not have permissions)
* Select the user that you want to add and click **Add**<br>

Learn more:

  * [Add a Co-Administrator](https://docs.microsoft.com/azure/role-based-access-control/classic-administrators#add-a-co-administrator)
  * [Remove a co-administrator](https://docs.microsoft.com/azure/role-based-access-control/classic-administrators#remove-a-co-administrator)
  * [Change the Service Administrator](https://docs.microsoft.com/azure/role-based-access-control/classic-administrators#change-the-service-administrator)
  * [View the Account Administrator](https://docs.microsoft.com/azure/role-based-access-control/classic-administrators#view-the-account-administrator)
  * [Manage access using RBAC and Azure portal](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal)

**Add/Delete users using Azure Active Directory**

You can add new users or delete existing users from your Azure Active Directory (Azure AD) organization:

* To add a new user, sign in to the [Azure portal](https://portal.azure.com/) as a User administrator for the organization
* Select **Azure Active Directory**, select **Users** and then select **New user**
* On the **User** page, fill out the required information. Select Create. The user is created and added to your Azure AD tenant.

Learn more:

  * [Add a new user](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory#add-a-new-user)
  * [Delete a user](https://docs.microsoft.com/azure/active-directory/fundamentals/add-users-azure-active-directory#delete-a-user)
  * [Add or update a user's profile information using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-profile-azure-portal)

**Unable to view resources/services**

1. Please log out of all the active azure sessions. Follow the below steps [here](http://www.thewindowsclub.com/launch-start-private-browsing) for in- Private session of the internet explorer, if using google chrome please use the incognito mode of the browsing.
2. You could also try to Refresh browser, use another browser, delete cache cookies if above doesn't work

## **Recommended Documents**

* [What is role-based access control (RBAC)?](https://docs.microsoft.com/azure/role-based-access-control/overview)
* [Understand the different roles in Azure](https://docs.microsoft.com/azure/role-based-access-control/rbac-and-directory-admin-roles)
* [Administrator role permissions in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles)
* [Tutorial: Grant access for a user using RBAC and the Azure portal](https://docs.microsoft.com/azure/role-based-access-control/quickstart-assign-role-user-portal)
* [Troubleshoot RBAC in Azure](https://docs.microsoft.com/azure/role-based-access-control/troubleshooting)
* [Organize your resources with Azure management groups](https://docs.microsoft.com/azure/azure-resource-manager/management-groups-overview)
* [How to request copy of Azure invoice via email](https://azure.microsoft.com/blog/azure-email-invoices/)
* [How to add, update or remove a credit or debit card from Azure](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Manage (Reactivate/Cancel/Switch) subscription](https://docs.microsoft.com/azure/billing/billing-subscription-become-disable)
