<properties pageTitle="I only used free services"
	description="I only used free services"
	service="Microsoft.Billing"
	resource=""
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783411,32783424"
	resourceTags=""
	productPesIds="17325"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a23f2a5d-82ee-45cd-80cc-94437039afcb"
	ownershipId="ASMS_Billing"
/>
# I only used free services

## **Recommended Steps**

### **There are several reasons why you might find charges on your free account and free services usage**

**Avoid charges with your Azure free account**

Eligible new users get $200 of Azure credit for the first 30 days and a limited quantity of free services for 12 months with your Azure free account. To learn about limits of free services, see the Azure free account FAQ. As long as you have unexpired credit or you use only free services within the limits, you're not charged.

For more information on how to avoid charges see, [Avoid charges with your Azure free account](https://docs.microsoft.com/azure/cost-management-billing/manage/avoid-charges-free-account).

### **Reasons you can incur charges on your Azure free account**

**Your credit runs out or is expired**

Your subscription and services are disabled when your credit runs out or expires at the end of 30 days. To continue using Azure services, you must upgrade your account. For more information, see [Upgrade your Azure free account](https://docs.microsoft.com/azure/cost-management-billing/manage/upgrade-azure-subscription).

**Usage exceeds the limits of free service**

You get a limited quantity of free services each month with your Azure free account. The free quantity expires at the end of the month and doesn't roll over to the next month. For more information, see [Usage exceeds the limits of free services](https://docs.microsoft.com/azure/cost-management-billing/manage/avoid-charges-free-account#usage-exceeds-the-limits-of-free-services).

**You used some services that aren’t free**

After you've upgraded your account, you get charged pay-as-you-go rates for using services that aren't included for free with your Azure free account. Only certain tiers within a service are included for free. To learn about services included with your free account, see the [Azure free account FAQ](https://azure.microsoft.com/free/free-account-faq/). You can check your service usage in the Azure portal. To learn more, see [Plan and control expenses](https://docs.microsoft.com/azure/cost-management-billing/cost-management-billing-overview#plan-and-control-expenses).

**You reached the end of your free 12 months**

Your free services and quantities expire at the end of 12 months. You can find out when your free services expire in the Azure portal.

1. Sign in to the Azure portal
2. In the left navigation area, select **All services**
3. Select **Subscriptions**
4. Select the subscription that was created when you signed up for free account
5. Scroll down to find free services grid. Select the tooltip located on the top left of the grid.

Microsoft will send you an email notifying you when it's time to upgrade.

After your free services and quantities expire, you're charged pay-as-you-go rates for any services you're using. You can use the Azure portal to delete the resources for the services that you don't use. If you don’t intend to use any Azure service, you can cancel your subscription.

### **Understand your bill**

If you believe you have unexpected charges under your Free Trial account, follow these steps to get more understanding about your bill.

1. Get the `Invoice ID` from the invoice pdf. This should also be available in the invoice email that account admin would have received.
2. Search for this invoice number in the Azure portal to find the **Invoice** link. If you don't have the permission to view invoices, you might receive a message saying **‘Either the invoice doesn't exists or you don't have access to view the invoice.'** See [manage billing access](https://docs.microsoft.com/azure/cost-management-billing/manage/manage-billing-access#opt-in) to determine which roles can access the invoice.
3. Select the **Invoice** link to show details of the invoice in the portal.<br> 
The data under **Billing summary** should exactly match the charges details in your invoice.

4. Select **View in Cost Analysis**. 
This opens the detailed cost analysis view of the invoice showing the different resources with their associated fields, such as service type, and so on.

5. Select the **resource** link to view details of the SKU information. <br>
   - If a free SKU is not used and if $200 Azure credit is finished, a charge will get incurred.   
   - If you opted for a support plan when you upgraded, the cost of that support plan will show in the previous view. 
   - If you wish to cancel your support plan, see [Cancel a support plan](https://azure.microsoft.com/resources/knowledge-center/how-do-i-change-or-cancel-my-azure-support-plan/). 
   - For complete list of eligible services in the free trial account, see [Free services](https://azure.microsoft.com/free/free-account-faq/).

6. To see cost where the publisher is not Azure, group by **Publisher Type**. <br>
   All resources where publisher is not Azure is charged. We have a lot of offerings in Azure Market Place from external publishers. For list of marketplace offering with the publisher info, see [Azure marketplace](https://azuremarketplace.microsoft.com/marketplace/).

7. If you want to get rid of the future cost, select the **resource** and delete the resource using [instructions to manage resources](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resources-portal#open-resources).<br>
   Note that you need to have permissions to the subscription/resource. If you wish to cancel a subscription, see **Cancel subscription**.
In case of deletion, you might still see a charge for the resource in the next invoice. This charge would map to the usage incurred during the billing period for the period between 5th of the month and date when you deleted the source.

## **Recommended Documents**

* [Avoid charges with your Azure free account](https://docs.microsoft.com/azure/cost-management-billing/manage/avoid-charges-free-account)
* [Monitor and track Azure free service usage](https://docs.microsoft.com/azure/cost-management-billing/manage/check-free-service-usage)
* [Tutorial: Review your individual Azure subscription bill](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill)
