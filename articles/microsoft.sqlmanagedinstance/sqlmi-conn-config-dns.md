<properties
	pageTitle="How to questions: DNS configuration"
	description="How to questions: DNS configuration"
	infoBubbleText="DNS configuration"
	service="microsoft.sql"
	resource="managedinstances"
	authors="srdan-bozovic-msft,vitomaz-msft"
	authoralias="srbozovi,vitomaz"
	ms.author="srbozovi,vitomaz"
	displayOrder=""
	articleId="sqlmi-conn-config-dns"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748004"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	ownershipId="AzureData_AzureSQLMI"
/>

# DNS configuration

## **Recommended Steps**

There are a few scenarios (for example, db mail, linked servers to other SQL Server instances in your cloud or hybrid environment) that require private host names to be resolved from SQL Managed Instance. For these cases, you'll need to configure a custom DNS inside Azure. See [Configure a custom DNS for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/custom-dns-configure) for details.

**Updating virtual network DNS servers will not affect SQL Managed Instance immediately** <br>
If this change is implemented after a [virtual cluster](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview#virtual-cluster-connectivity-architecture) hosting Managed Instance is created, you'll need to synchronize DNS servers setting on the virtual cluster with the virtual network configuration. See [how to synchronize virtual network DNS servers setting on SQL Managed Instance virtual cluster](https://docs.microsoft.com/azure/azure-sql/managed-instance/synchronize-vnet-dns-servers-setting-on-virtual-cluster) for more details.

For questions on how to change a managed instance name or DNS zone prefix, see [naming conventions](https://docs.microsoft.com/azure/azure-sql/managed-instance/frequently-asked-questions-faq#naming-conventions) in our frequently asked questions (FAQ).
