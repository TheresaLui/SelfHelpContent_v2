<properties
	pageTitle="unexpectedcharges-understand a charge"
	description="unexpectedcharges-understand a charge"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32680680"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake"
	articleId="unexpectedcharges-understandacharge"
	ownershipId="ASMS_Billing"
/>

# Unexpected Charges-understand a charge

**The Azure Free Account** offer includes $200 of Azure credits (to be used within the first 30 days of sign-up) and 12 months of select free services (subject to change). This offer is limited to one enrollment per eligible customer and cannot be combined with any other offer unless otherwise permitted by Microsoft.<br>

Within 30 days of sign-up or upon exhaustion of the customer’s credits (whichever occurs first), the customer must upgrade to a Pay-As-You-Go account by removing the Spending Limit. This allows continued use of the Azure Free Account for the remaining 11 months. After the customer has upgraded, usage outside the initial credits and select free services will be billed at Pay-As-You-Go rates. If the customer elects not to upgrade, the Free Account subscription will be disabled. Learn more: [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)

The users detailed usage (CSV report) shows a list of the quantity of each resource that was consumed within the current billing period. The file shows cumulative monthly usage and a breakdown of daily usage for each resource. Learn more:

  * [Understanding Your Azure Bill](http://azure.microsoft.com/support/understand-your-bill/)
  * [Understand Detailed Usage Charges](http://azure.microsoft.com/support/understand-your-bill/#understand-detailed-usage-charges)
  * [Download or view Azure billing invoice and daily usage data](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)

**Note**: If you cancel your subscription/resource in the middle of your billing cycle, you might still see a charge which would be for any usage in the previous month. Example, if your billing cycle was from the 26th of every month to the 25th of the next month & you suspended the subscription on the 23rd, which is 28 days into the billing cycle for June, you might see a charge for the 28 days of use. If you see a charge in spite of cancelling a subscription please make sure, you don’t have any other support plans which is causing the charge. If you do, please go ahead and cancel the plan.<br>

**Windows and SQL software** is charged separately with Azure reserved instances. [Learn more](https://docs.microsoft.com/azure/cost-management-billing/reservations/reserved-instance-windows-software-costs)

**Azure Bizspark Subscription**: A BizSpark subscription had a validity of 2 years.  Once the validity of the subscription ends, it is converted to Pay-As-You-Go subscription. Learn more: [Azure Bizspark subscription](https://azure.microsoft.com/offers/ms-azr-0064p/)

For **Storage** usage, the user can enable Storage Analytics. Enabling Storage Analytic logs gives user the ability to have per-transaction logging. The logs are quite detailed and users can do end-to-end tracing and debugging on their own. More details are available at the below links:

  * [Storage Analytics](http://msdn.microsoft.com/library/windowsazure/hh343270.aspx )
  * [Windows Azure Storage Logging: Using Logs to Track Storage Requests](https://blogs.msdn.microsoft.com/windowsazurestorage/?m=20118)
  * [Monitor a storage account in the Azure portal](http://azure.microsoft.com/documentation/articles/storage-monitor-storage-account/)<br>
  
For **network-related usage**, the user can use a network capture tool such as Microsoft Network Monitor or a simple HTTP capture tool like Fiddler:

  * [Network Monitor](http://www.microsoft.com/download/details.aspx?id=4865 )
  * [Fiddler](http://www.telerik.com/fiddler) (NOTE: this tool is not supported by Microsoft)<br>
  
* For issues related to the **Virtual Machines running a Windows OS image**, the host OS Event Logs can be used: [Windows Event Logs](https://docs.microsoft.com/windows/win32/eventlog/about-event-logging)
* For **PaaS deployments**, enable diagnostics in the application: [Enable diagnostics in a cloud service](https://azure.microsoft.com/documentation/articles/cloud-services-dotnet-diagnostics/)
* For **IaaS deployments**: [Enable diagnostics logging for apps](https://docs.microsoft.com/azure/app-service/troubleshoot-diagnostic-logs)

## **Recommended Documents**

* [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/)
* [Azure offers: https](//azure.microsoft.com/support/legal/offer-details/)
* [Cancel subscription](https://docs.microsoft.com/azure/billing/billing-how-to-cancel-azure-subscription)
* [Manager Resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-portal)
* [Download usage and invoices](https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date)
* [Pricing overview](https://azure.microsoft.com/pricing/)
* [Add/Update Credit Card](https://docs.microsoft.com/azure/billing/billing-how-to-change-credit-card)
* [Update/change profile information](https://docs.microsoft.com/azure/billing/billing-how-to-change-azure-account-profile)
