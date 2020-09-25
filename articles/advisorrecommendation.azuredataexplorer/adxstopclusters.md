<properties
    pageTitle="Stop Azure Data Explorer clusters to reduce cost and keep its data."
    description="Stop Azure Data Explorer clusters to reduce cost and keep its data."
    authors="raldaba"
    ms.author="aoaft"
    articleId="7b56698e-2d5f-49b8-aef5-e146a9056a1c_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureOptimizationAutomation_AORec"
/>
# The following ADX clusters have been identified as candidates for stopping
---
{
  "recommendationOfferingId": "7c694977-1723-420b-9bb9-1f958e642206",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "040e5a2c-6a2a-4e3a-8a7e-8ad320473a2f",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('CustomerPublish').AzureAdvisor_ADX_StopClustersReco",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/clusters",
  "recommendationFriendlyName": "Stop ADX clusters to reduce cost and keep its data",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aoaft@microsoft.com",
    "icm": {
      "routingId": "AORECOMMENDATIONS\\Triage",
      "service": "AO Recommendations",
      "team": "Triage"
    },
    "serviceTreeId": "a3db6cf3-640c-4340-8381-108d31853b7f"
  },
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe",
    "9c14bff5-1bda-4de6-a74f-4c3caa370570"
  ],
  "recommendationTimeToLive": 86400,
  "version": 2.3,
  "learnMoreLink": "https://aka.ms/adxstopclusters",
  "description": "(PREVIEW) Stop Azure Data Explorer clusters to reduce cost and keep its data",
  "longDescription": "Your cluster has data but is not being used. Stop the cluster to reduce cost and still save the data. If the data is not needed, consider deleting the cluster to increase your savings.",
  "potentialBenefits": "Optimize cost",
  "actions": [
	{
      "actionId": "a9c35fc9-f465-4434-be8f-6636e6be21f5",
      "description": "Stop your cluster",
      "actionType": "Blade",
	  "extensionName": "Microsoft_Azure_Kusto",
      "bladeName": "ClusterOverviewBladeViewModel",
      "metadata": {
        "id": "{resourceId}"
      }
	}
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "76e92648-475e-437c-a93d-f04275f8cdae",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider stopping your cluster to save on cost",
  "additionalColumns": [
    {
      "name": "currentConfig",
      "title": "Current Configuration"
    },
	{
      "name": "observationStartTime",
      "title": "Observation Start Time"
    },
	{
      "name": "observationEndTime",
      "title": "Observation End Time"
    }
  ],
  "testData": "08ed568c-822f-4f2d-9327-e79bde1d18c1,/subscriptions/08ed568c-822f-4f2d-9327-e79bde1d18c1/resourceGroups/Cerebro-dev/providers/Microsoft.Kusto/clusters/cerebrodev,2.3,\"{\"\"clusterName\"\":\"\"cerebrodev\"\",\"\"currentConfig\"\":\"\"Mock Standard_D11_v2 - 2 Instances\"\",\"\"observationStartTime\"\":\"\"2020-08-18T20:40:28.1128748Z\"\",\"\"observationEndTime\"\":\"\"2020-09-17T20:40:28.1128748Z\"\",\"\"savingsAmount\"\":\"\"105.04\"\",\"\"annualSavingsAmount\"\":\"\"1260.48\"\",\"\"savingsCurrency\"\":\"\"USD\"\"}\"",
  "remediation": [
    {
      "httpMethod": "POST",
      "uri": "{armEndpoint}{resourceId}/stop?api-version=2019-11-09",
      "actionId": "a9c35fc9-f465-4434-be8f-6636e6be21f5",
      "implication": "Your cluster will go offline",
      "documentationLink": "https://aka.ms/adxstopclustersapi",
      "asyncRequestDetails": {
        "header": "Azure-AsyncOperation",
        "pollingFrequencyInSeconds": 30,
        "terminatingCondition": {
          "timeOutInSeconds": 1800,
          "httpStatusCode": 200
        }
      }
    }
  ],
  "costSavingInfo": "*Your actual yearly savings may vary. The yearly saving that is presented is based on 'pay as you go' prices. The potential saving does not take into consideration Azure Reserved VM Instances (RIs) billing discounts you may have."
}
---
