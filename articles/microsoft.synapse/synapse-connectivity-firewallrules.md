<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "workspaces"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738771"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Connectivity/Firewall rules"
	description = "Connectivity/Firewall rules"
	articleId = "synapse-connectivity-firewallrules"
	authors = "saltug"
	ms.author = "saltug"
/>

# Connectivity/Firewall rules

## **Recommended Steps**

[IP firewall rules](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall) grant or deny access to your Synapse workspace based on the originating IP address of each request. You can configure IP firewall rules for your workspace. IP firewall rules configured at the workspace level apply to all public endpoints of the workspace (SQL pools, SQL on-demand, and Development).

Diagnose Azure Synapse Studio connectivity issues with [```Test-AzureSynapse``` PowerShell script](https://docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio-powershell).

## **Recommended Documents**

* [Create and manage IP firewall rules](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall#create-and-manage-ip-firewall-rules)
* [Connecting to Synapse from your own network](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall#connecting-to-synapse-from-your-own-network)
* [Managed workspace VNet](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-vnet)
* [Managed private endpoint](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-private-endpoints)
* [Connect to your Azure Synapse workspace using private links](https://docs.microsoft.com/azure/synapse-analytics/security/how-to-connect-to-workspace-with-private-links#step-1-open-your-azure-synapse-workspace-in-azure-portal)
