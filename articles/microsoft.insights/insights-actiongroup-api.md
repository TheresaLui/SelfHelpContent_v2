<properties
	pageTitle="I am having issues managing Action groups with API/CLI"
	description="I am having issues managing Action groups with API/CLI"
	infoBubbleText=""
	service="microsoft.insights"
	resource="actiongroups"
	authors="snehithm,dkamstra"
	ms.author="snmuvva,dukek"
	displayOrder="8"
	articleId="insights-actiongroup-api"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629614"
	resourceTags=""
	productPesIds="15454"
	cloudEnvironments="public,fairfax, usnat, ussec"
	ownershipId="AzureMonitoring_ActionGroup"
/>

# I am having issues managing metric alerts with API/CLI

Most alerts in Azure Monitor use [Action Groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups) as the notification delivery mechanism.

## **Recommended Steps**

If you are running into issues creating/updating/deleting Action groups using REST API or Azure command line interface (CLI), the following steps may help resolve the issue:

1. Review the [REST API guide](https://docs.microsoft.com/rest/api/monitor/actiongroups/) to verify you are passing the all the parameters correctly
2. Review the [CLI guide](https://docs.microsoft.com/cli/azure/monitor/action-group?view=azure-cli-latest) for samples and usage
