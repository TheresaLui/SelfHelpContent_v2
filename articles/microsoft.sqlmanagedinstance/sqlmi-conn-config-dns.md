<properties
	pageTitle="How to questions: DNS configuration"
	description="How to questions: DNS configuration"
	infoBubbleText="DNS configuration"
	service="microsoft.sql"
	resource="managedinstances"
	authors="vitomaz-msft"
	authoralias="vitomaz"
	ms.author="vitomaz"
	displayOrder=""
	articleId="sqlmi-conn-config-dns"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32748004"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	ownershipId="AzureData_AzureSQLMI_Connectivity"
/>

# DNS configuration

There are a few scenarios (for example, db mail, linked servers to other SQL Server instances in your cloud or hybrid environment) that require private host names to be resolved from SQL Managed Instance. In this case, you need to configure a custom DNS inside Azure. See [Configure a custom DNS for Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/managed-instance/custom-dns-configure) for details.

**Updating virtual network DNS servers won't affect SQL Managed Instance immediately**.  
If this change is implemented after [virtual cluster](https://docs.microsoft.com/azure/azure-sql/managed-instance/connectivity-architecture-overview#virtual-cluster-connectivity-architecture) hosting Managed Instance is created you'll need to synchronize DNS servers setting on the virtual cluster with the virtual network configuration. See [how to synchronize virtual network DNS servers setting on SQL Managed Instance virtual cluster](https://docs.microsoft.com/azure/azure-sql/managed-instance/synchronize-vnet-dns-servers-setting-on-virtual-cluster) for more details.