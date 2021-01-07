<properties
    pageTitle="vSAN Capacity Utilization"
    description="vSAN capacity warnings"
    ms.author="chetaks"
    articleId="c397af14-f2eb-454b-8419-2a8e7d9aef8a"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="CloudES_AzureSupportCenterTest"
/>
# vSAN Capacity Warning
---
{
  "recommendationOfferingId": "",
  "recommendationOfferingName": "vSAN Capacity Utilization",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c397af14-f2eb-454b-8419-2a8e7d9aef8a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://skylink.kusto.windows.net').database('AVSProd').tenanthealth",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/VirtualMachines",
  "recommendationFriendlyName": "vSANCapacity",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "chetaks@microsoft.com",
    "icm": {
      "routingId": "mdm://tenanthealth",
      "service": "Azure VMware Solution",
      "team": "Triage"
    },
    "serviceTreeId": "VMWAREVIRTUSTREAM\Triage"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://www.vmware.com/my/products/vsan.html",
  "description": "vSAN Capacity Warning",
  "longDescription": "Your vSAN capacity utilization has reached 65%. The cluster utilization is required to remain below the 75% critical threshold for SLA compliance. Please add nodes or adjust your VM workloads to not exceed 75% utilization and fall out of SLA compliance.
",
  "potentialBenefits": "Maintain the health and performance of your vSAN operations",
  "actions": [
    {
      "actionId": "",
      "description": "",
      "actionType": "",
      "extensionName": "",
      "bladeName": "",
      "metadata": {},
      "documentLink": ""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "",
      "actionType": "",
      "extensionName": "",
      "bladeName": "",
      "metadata": {},
      "documentLink": ""
    }
  },
  "displayLabel": "Your vSAN utilization is high and the Private Cloud may soon fall out of SLA compliance",
  "additionalColumns": [],
  "tip": "",
  "costSavingInfo": "",
  "testData": ""
}
---
