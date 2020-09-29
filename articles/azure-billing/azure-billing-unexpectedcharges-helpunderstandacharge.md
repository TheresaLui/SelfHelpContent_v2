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
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="unexpectedcharges-understandacharge"
	ownershipId="ASMS_Billing"
/>

# Unexpected Charges-understand a charge

**Understand charges on an Azure free account**<br>
Azure free trial account is only for 1 month and once it is upgraded to pay-g there will be 12 month free services. The Azure free account includes free access to the most popular Azure products for 12 months, $200 credit to spend for the first 30 days of sign up, and access to more than 25 products that are always free. If you are seeing a charge, it is likely possible that it is not one of the listed products that are available monthly, for free: [Products available monthly for free under Azure free account](https://azure.microsoft.com/free/free-account-faq/)<br>

**Note**: You would need to upgrade to [Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-0003p/) after the first 30 days in order to continue using the Free Account for the remaining 11 months and you would not be charged if you stayed within the free service limits.

**Understand charges on your Bill/Invoice?**<br>

**Customer Led (WD)**

* To help review and understand your bill, please refer to: [Tutorial: Review your individual Azure Bill](https://docs.microsoft.com/azure/cost-management-billing/understand/review-individual-bill)
* Understand terms on your invoice: [Azure invoice terms explained](https://docs.microsoft.com/azure/cost-management-billing/understand/understand-invoice)
* Understand terms on Azure Usage charges: [Usage terms explained](https://docs.microsoft.com/azure/cost-management-billing/understand/understand-usage)
* To obtain a PDF of your invoice and a copy of your detailed daily usage file (.CSV): [Get invoice and usage data](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date)

**Note**: If you cancel your subscription/resource in the middle of your billing cycle, you might still see a charge which would be for any usage in the previous month. Example, if your billing cycle was from the 26th of every month to the 25th of the next month & you suspended the subscription on the 23rd, which is 28 days into the billing cycle for June, you might see a charge for the 28 days of use. If you see a charge in spite of cancelling a subscription please make sure, you don’t have any other support plans which is causing the charge. If you do, please go ahead and cancel the plan.

**Microsoft Customer Agreement (MCA)**

[How to Check access to a Microsoft Customer Agreement?](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date#check-access-to-a-microsoft-customer-agreement)

* To help review and understand your bill, please refer to: [Tutorial: Review your Microsoft Customer Agreement invoice](https://docs.microsoft.com/azure/cost-management-billing/understand/review-customer-agreement-bill)
* Understand terms on your invoice: [Microsoft Customer Agreement Invoice terms explained](https://docs.microsoft.com/azure/cost-management-billing/understand/mca-understand-your-invoice)
* Understand terms on Azure Usage charges: [Microsoft Customer Agreement Usage Terms explained](https://docs.microsoft.com/azure/cost-management-billing/understand/mca-understand-your-usage)
* If you are a [Microsoft Customer Agreement](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date#check-access-to-a-microsoft-customer-agreement), you can download usage in the [Azure portal](https://portal.azure.com/)

**Microsoft Partner Agreement (MPA)**

* To help review and understand your bill, please refer to: [Tutorial:Review your Microsoft Partner Agreement invoice](https://docs.microsoft.com/azure/cost-management-billing/understand/review-partner-agreement-bill)
* Understand terms on your invoice: [Terms in Microsoft Partner Agreement invoice explained](https://docs.microsoft.com/azure/cost-management-billing/understand/mpa-invoice-terms)

**Enterprise Agreement (EA)**

* To help review and understand your bill, please refer to: [Understand your Azure Enterprise Agreement bill](https://docs.microsoft.com/azure/cost-management-billing/understand/review-enterprise-agreement-bill)
* If you're an Azure customer with an Enterprise Agreement (EA customer), you can't download your organization's invoices. Invoices are sent to whoever is set up to receive invoices for the enrollment, you can download usage in the [Azure portal](https://portal.azure.com/)

**Cloud Solution Provider (CSP)**

* Learn more on how billing works in Azure Cloud Solution Provider (Azure CSP) program: [Azure CSP Billing](https://docs.microsoft.com/azure/cloud-solution-provider/billing/azure-csp-billing-overview)
* Learn on reading and understanding your CSP bill: [Azure CSP invoice](https://docs.microsoft.com/azure/cloud-solution-provider/billing/azure-csp-invoice)

**Azure Reservation**: **Windows and SQL software** is charged separately with Azure reserved instances. [Learn more](https://docs.microsoft.com/azure/cost-management-billing/reservations/reserved-instance-windows-software-costs)

**Azure Bizspark Subscription**: A BizSpark subscription had a validity of 2 years.  Once the validity of the subscription ends, it is converted to Pay-As-You-Go subscription. Learn more: [Azure Bizspark subscription](https://azure.microsoft.com/offers/ms-azr-0064p/)

For **Storage** usage, the user can enable Storage Analytics. Enabling Storage Analytic logs gives user the ability to have per-transaction logging. The logs are quite detailed and users can do end-to-end tracing and debugging on their own. More details are available at the below links:

* [Storage Analytics](http://msdn.microsoft.com/library/windowsazure/hh343270.aspx )
* [Windows Azure Storage Logging: Using Logs to Track Storage Requests](https://blogs.msdn.microsoft.com/windowsazurestorage/?m=20118)
* [Monitor a storage account in the Azure portal](http://azure.microsoft.com/documentation/articles/storage-monitor-storage-account/)<br>

For **network-related usage**, the user can use a network capture tool such as Microsoft Network Monitor or a simple HTTP capture tool like Fiddler:

* [Network Monitor](https://support.microsoft.com/help/933741/information-about-network-monitor-3)
* [Fiddler](http://www.telerik.com/fiddler) NOTE: this tool is not supported by Microsoft<br>

For issues related to the **Virtual Machines running a Windows OS image**, the host OS Event Logs can be used: [Windows Event Logs](https://docs.microsoft.com/windows/win32/eventlog/about-event-logging)

For **PaaS deployments**, enable diagnostics in the application: [Enable diagnostics in a cloud service](https://azure.microsoft.com/documentation/articles/cloud-services-dotnet-diagnostics/)

For **IaaS deployments**: [Enable diagnostics logging for apps](https://docs.microsoft.com/azure/app-service/troubleshoot-diagnostic-logs)

## **Recommended Documents**

* [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/)
* [Azure offers](https://azure.microsoft.com/support/legal/offer-details/)
* [Cancel subscription](https://docs.microsoft.com/azure/cost-management-billing/manage/cancel-azure-subscription)
* [Manager Resources](https://docs.microsoft.com/azure/azure-resource-manager/management/manage-resources-portal)
* [Download usage and invoices](https://docs.microsoft.com/azure/cost-management-billing/manage/download-azure-invoice-daily-usage-date)
* [Pricing overview](https://azure.microsoft.com/pricing/)
* [Add/Update Credit Card](https://docs.microsoft.com/azure/cost-management-billing/manage/change-credit-card)
* [Update/change profile information](https://docs.microsoft.com/azure/cost-management-billing/manage/change-azure-account-profile)
