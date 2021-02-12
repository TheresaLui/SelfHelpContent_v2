<properties
    pageTitle="Action required: Migrate your A8–A11 HDInsight cluster before 1 March 2021"
    description="Action required: Migrate your A8–A11 HDInsight cluster before 1 March 2021"
    authors="xunwei"
    ms.author="xunwei"
    articleId="11741e31-c2ca-4739-92de-04ff7eca697c_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Action required: Migrate your A8–A11 HDInsight cluster before 1 March 2021
---
{
  "recommendationOfferingId": "e24dace6-5068-4c13-b6b7-88b7b6e8a577",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "11741e31-c2ca-4739-92de-04ff7eca697c",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').VMDeprecation",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "VMDeprecation",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdicp@microsoft.com",
    "icm": {
      "routingId": "MDM://ControlPlane",
      "service": "HDInsight",
      "team": "Control Plane"
    },
    "serviceTreeId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://azure.microsoft.com/updates/a8-a11-azure-virtual-machine-sizes-will-be-retired-on-march-1-2021/",
  "description": "Action required: Migrate your A8–A11 HDInsight cluster before 1 March 2021",
  "longDescription": "You're receiving this notice because you have one or more active A8, A9, A10 or A11 HDInsight cluster. The A8-A11 virtual machines (VMs) will be retired in all regions on 1 March 2021. After that date, all clusters using A8-A11 will be deallocated. Migrate your affected clusters to another HDInsight supported VM (https://azure.microsoft.com/pricing/details/hdinsight/) before that date. For more details, see 'Learn More' link or contact us at askhdinsight@microsoft.com",
  "actions": [
    {
      "actionId": "c6359c0c-6a5c-4f03-862d-98ef5b52b1eb",
      "description": "Migrate your affected clusters to another HDInsight supported VM before that date.",
      "actionType": "Document",
      "documentLink": "https://azure.microsoft.com/resources/hpc-migration-guide/"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "cf6d80d0-6410-489b-8b34-727145e25886",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Action required: Migrate your A8–A11 HDInsight cluster before 1 March 2021",
  "additionalColumns": [],
  "tip": "Action required: Migrate your A8–A11 HDInsight cluster before 1 March 2021",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-shc/providers/Microsoft.HDInsight/clusters/swstorm"
}
---
