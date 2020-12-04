<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783925"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Connectivity/Synapse Studio"
    description = "Connectivity/Synapse Studio"
    articleId = "synapse-cs-connectivity-synapsestudio.md"
    ms.author = "saltug"
/>

# Connectivity/Synapse Studio

## **Recommended Steps**

* Learn [how to troubleshoot](https://docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio#troubleshooting-steps) Synapse Studio

* Diagnose connectivity issues using this [PowerShell script](https://docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio-powershell)

* Confirm Synapse Studio is able to access all the required endpoints:

   - Make sure that the firewall on your network and local computer allows outgoing communication on TCP ports 80, 443 and 1443 for Synapse Studio
   - Allow outgoing communication on UDP port 53 for Synapse Studio
   - To connect using tools such as SSMS and Power BI, you must allow outgoing communication on TCP port 1433
   - If you're using the default Redirect connection policy setting, you may need to allow outgoing communication on additional ports

* Test access with different browsers and disable any pop-up blockers and plugins

* Investigate issues related to Security and Permissions:

	- [Workspaces, data, and pipelines](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control)
   	- [Managed identities](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-identity)
	- [Database access](https://docs.microsoft.com/azure/azure-sql/database/logins-create-manage?toc=%2Fazure%2Fsynapse-analytics%2Ftoc.json&bc=%2Fazure%2Fsynapse-analytics%2Fbreadcrumb%2Ftoc.json)
	
## **Recommended Documents**

* [Launch Synapse Studio](https://docs.microsoft.com/azure/synapse-analytics/quickstart-synapse-studio#launch-synapse-studio)

* [Connect to Synapse from your own network](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall#connect-to-synapse-from-your-own-network)

* [Synapse Workspace Pools and On Demand Inaccessible](https://techcommunity.microsoft.com/t5/azure-synapse-analytics/synapse-workspace-pools-and-on-demand-inaccessible/ba-p/1403485)

 