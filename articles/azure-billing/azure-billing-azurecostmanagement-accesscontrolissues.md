<properties
	pageTitle="access control issues"
	description="access control issues"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32615278"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="public"
/>

# Acess Control Issues

You can grant access for Azure billing information to members of your team by assigning one of the following user roles to your subscription: Account Administrator, Service Administrator, Co-administrator, Owner, Contributor, Reader, and Billing Reader. They would have access to billing information in the [Azure portal](https://portal.azure.com), and they can use the Billing APIs to programmatically get invoices (once opted-in) and usage details.

**How to allow additional users to access invoices**

1. As the Account Administrator, select your subscription from the [Subscriptions blade](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) in Azure portal<br>
2. Select Invoices and then Access to invoices.<br>
3. Turn On the access followed by saving the changes, to allow users in subscription scoped roles to download invoice.<br>
4. The Account Administrator can also configure to have invoices sent via email. To learn more, see [Get your invoice in email](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date).<br>

**How to add users to the Billing Reader role**

1. Select your subscription from the [Subscriptions blade](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade) in Azure portal.<br>
2. Select Access control (IAM) and then click **Add**.<br>
3. Choose Billing Reader in the Select a role page.<br>
4. Type the email for the user you want to invite, then click **OK** to send the invitation.<br>
5. Follow instructions in the invite email to log in as a Billing Reader.<br>
Learn more : [Grant access to Billing](https://docs.microsoft.com/azure/billing/billing-manage-access#opt-in)

## **Recommended documents**

* [What is Azure Cost Management ?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt)<br>
* [Azure Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [Explore and analyze costs with Cost Analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management REST API](https://docs.microsoft.com/rest/api/cost-management/)<br>
* [Azure Consumption REST API](https://docs.microsoft.com/rest/api/consumption/)<br>
* [Azure Cost Management - Pricing](https://azure.microsoft.com/pricing/details/cost-management/)<br>
