<properties
    pageTitle="vSAN Capacity Utilization"
    description="vSAN capacity warnings"
    ms.author="chetaks"
    articleId="eeb4ed3e-4e9b-40b4-84fb-5514d0be0eda_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="AzureDedicated_Networking"
/>
# vSAN Capacity Warning
---
{
  "recommendationOfferingId": "ee4d26c1-13da-47fa-af18-02c12ecf15a9",
  "recommendationOfferingName": "Azure VMware Solution",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "eeb4ed3e-4e9b-40b4-84fb-5514d0be0eda",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://skylink.kusto.windows.net').database('AVSProd').clusterUsed75",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.AVS/privateClouds",
  "recommendationFriendlyName": "vSANCapacity",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "chetaks@microsoft.com",
    "icm": {
      "routingId": "mdm://tenanthealth",
      "service": "Azure VMware Solution",
      "team": "Triage"
    },
    "serviceTreeId": "ee4d26c1-13da-47fa-af18-02c12ecf15a9"
  },
  "ingestionClientIdentities": [],
  "version": 1.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/azure-vmware/concepts-private-clouds-clusters",
  "description": "vSAN capacity utilization has crossed critical threshold",
  "longDescription": "Your vSAN capacity utilization has reached 75%. The cluster utilization is required to remain below the 75% critical threshold for SLA compliance. Please add new nodes to VSphere cluster to increase capacity or delete VMs to reduce consumption or adjust VM workloads",
  "potentialBenefits": "Maintain the health and performance of your vSAN operations",
  "actions": [
    {
      "actionId": "a3173c63-db87-414a-bf6d-683e2e97c4c1",
      "description": "Reduce your storage utilization to below 75%",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/azure-vmware/concepts-storage"
    }
  ],
  "displayLabel": "Your vSAN utilization is high and out of SLA compliance",
  "additionalColumns": [],
  "tip": "",
  "costSavingInfo": "",
  "testData": "1178f22f-6ce4-45e3-bd92-ba89930be5be,/subscriptions/1178f22f-6ce4-45e3-bd92-ba89930be5be/resourceGroups/shawnhu_test/providers/Microsoft.AVS/privateClouds/shawnhuAVStest"
}
---
