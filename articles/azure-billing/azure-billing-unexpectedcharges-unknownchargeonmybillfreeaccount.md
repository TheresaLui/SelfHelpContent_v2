<properties
	pageTitle="unexpectedcharges-i recieved new unknown charges on my bill"
	description="unexpectedcharges-i recieved new unknown charges on my bill"
	service="azure-billing"
	resource="billing"
	authors="lishepar"
	ms.author="lishepar"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32632931"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="unexpectedcharges-irecievedunknownchargeonmybill"
	ownershipId="ASMS_Billing"
/>

# <-- Unexpected Charges - I Recieved new unknown charges on my bill -->

## ** <-- Unexpected Charges - I recieved new unknown charges on my bill  --> **
<!--issueDescription-->
When the customer goes to the solutions page, the offer type associated with the account with filter only solutions that apply to them and present them in the solutions page.

<!--/issueDescription-->

**Understand charges on an Azure free account**<br>
Azure free trial account is only for 1 month and once it is upgraded to pay-g there will be 12 month free services. The Azure free account includes free access to the most popular Azure products for 12 months, $200 credit to spend for the first 30 days of sign up, and access to more than 25 products that are always free. If you are seeing a charge, it is likely possible that it is not one of the listed products that are available monthly, for free: [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)<br>
**Note**: You would need to upgrade to [Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-0003p/) after the first 30 days in order to continue using the Free Account for the remaining 11 months and you would not be charged if you stayed within the free service limits.

For **Storage** usage, the user can enable Storage Analytics. Enabling Storage Analytic logs gives user the ability to have per-transaction logging. The logs are quite detailed and users can do end-to-end tracing and debugging on their own. More details are available at the below links:

  * [Storage Analytics](http://msdn.microsoft.com/library/windowsazure/hh343270.aspx )
  * [Windows Azure Storage Logging: Using Logs to Track Storage Requests](https://blogs.msdn.microsoft.com/windowsazurestorage/?m=20118)
  * [Monitor a storage account in the Azure portal](http://azure.microsoft.com/documentation/articles/storage-monitor-storage-account/)<br>

For **network-related usage**, the user can use a network capture tool such as Microsoft Network Monitor or a simple HTTP capture tool like Fiddler:

  * [Network Monitor](http://www.microsoft.com/download/details.aspx?id=4865 )
  * [Fiddler](http://www.telerik.com/fiddler) (NOTE: this tool is not supported by Microsoft)<br>

* For issues related to the **Virtual Machines running a Windows OS image**, the host OS Event Logs can be used: [Windows Event Logs](https://docs.microsoft.com/windows/win32/eventlog/about-event-logging)
* For **PaaS deployments**, enable diagnostics in the application: [Enable diagnostics in a cloud service](https://azure.microsoft.com/documentation/articles/cloud-services-dotnet-diagnostics/)
* For **IaaS deployments**: [Enable diagnostics logging for apps](https://docs.microsoft.com/azure/app-service/troubleshoot-diagnostic-logs)

## **Recommended Documents**

* [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/)
* [Azure offers](https://azure.microsoft.com/support/legal/offer-details/)
* [Cancel subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/cancel-azure-subscription)
* [Manager Resources](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resources-portal)
* [Download usage and invoices](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date)
* [Pricing overview](https://azure.microsoft.com/pricing/)
* [Add/Update Credit Card](https://docs.microsoft.com/azure/cost-management-billing/manage/change-credit-card)
* [Update/change profile information](https://docs.microsoft.com/azure/cost-management-billing/manage/change-azure-account-profile)
