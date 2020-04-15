<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake"
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

[IP firewall rules](https://review.docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall?branch=release-ignite-arcadia) grant or deny access to your Synapse workspace based on the originating IP address of each request. You can configure IP firewall rules for your workspace. IP firewall rules configured at the workspace level apply to all public endpoints of the workspace (SQL pools, SQL on-demand, and Development).

Diagnose Azure Synapse Studio connectivity issues with [```Test-AzureSynapse``` PowerShell script](https://review.docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio-powershell?branch=release-ignite-arcadia).

## **Recommended Documents**

* [Create and manage IP firewall rules](https://review.docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall?branch=release-ignite-arcadia#create-and-manage-ip-firewall-rules)
* [Connecting to Synapse from your own network](https://review.docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall?branch=release-ignite-arcadia#connecting-to-synapse-from-your-own-network)
* [Managed workspace VNet](https://review.docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-vnet?branch=release-ignite-arcadia)
* [Managed private endpoint](https://review.docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-private-endpoints?branch=release-ignite-arcadia)
* [Connect to your Azure Synapse workspace using private links](https://review.docs.microsoft.com/azure/synapse-analytics/security/how-to-connect-to-workspace-with-private-links?branch=release-ignite-arcadia#step-1-open-your-azure-synapse-workspace-in-azure-portal)