<properties
    pageTitle="Enable Traffic Analytics to view insights into traffic patterns across Azure resources"
    description="Enable Traffic Analytics to view insights into traffic patterns across Azure resources"
    authors="nwta"
    ms.author="nwta"
    articleId="7c27d589-c7ed-47e1-8fe9-fe12ea81634a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="CloudNet_NetworkWatcher"
/>
# Enable Traffic Analytics to view insights into traffic patterns across Azure resources
---
{
  "recommendationOfferingId": "f2d7af08-7231-4add-8aa8-d0f7efdbefb5",
  "recommendationOfferingName": "Network Watcher",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "7c27d589-c7ed-47e1-8fe9-fe12ea81634a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://aztmmon.kusto.windows.net').database('NetWatcherDB').AzAdvisorPublicFlowLogs",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/networkSecurityGroups",
  "recommendationFriendlyName": "NSGFlowLogsenableTA",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "nwta@microsoft.com",
    "icm": {
      "routingId": "mdm://NWTACloudService/Severity3Errors",
      "service": "Network Watcher Traffic Analytics",
      "team": "Dev Team-IDC"
    },
    "serviceTreeId": "b6650569-6d2d-4278-8437-d10caff5b5c3"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/aa_enableta_learnmore",
  "description": "Enable Traffic Analytics to view insights into traffic patterns across Azure resources",
  "longDescription": "Traffic Analytics is a cloud-based solution that provides visibility into user and application activity in Azure. Traffic analytics analyzes Network Watcher network security group (NSG) flow logs to provide insights into traffic flow. With traffic analytics, you can view top talkers across Azure and non Azure deployments, investigate open ports, protocols and malicious flows in your environment and optimize your network deployment for performance. You can process flow logs at 10 mins and 60 mins processing intervals, giving you faster analytics on your traffic.",
  "potentialBenefits": "Identify top talkers, traffic hotspots, resource utilisation and security based on traffic patterns in NSG",
  "actions": [
    {
      "actionId": "8653faf2-963e-4efd-b66a-f9183e28d0ae",
      "description": "Turn on Traffic Analytics status in flow logs settings",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "FlowLogsExtendedDiagnosticsSettingsUpdateBlade",
      "metadata": {
		"flowLogsSettingsInputs":
		{
			"resourceId": "{resourceId}",
			"location": "{location}"
		}
	  }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0e241dda-e657-4a0d-9fea-a4106ddf5327",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "NetworkSecurityGroupBlade",
      "metadata": {
		"id": "{resourceId}"
	  }
    }
  },
  "displayLabel": "Enable Traffic Analytics for NSG",
  "additionalColumns": [],
  "tip": "* Use 10 mins processing interval for faster insights. * You can select Flog Logs version 2 to see bytes and packets per flow"
}
---
