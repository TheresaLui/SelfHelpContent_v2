<properties
    pageTitle="Delete and recreate your Azure Bastion resource"
    description="Delete and recreate your Azure Bastion resource"
    authors="bastionpm"
    ms.author="bastionpm"
    articleId="17ebccd8-1405-405c-8695-1981d115ffdc_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat",
    ownershipId="CloudNet_AzureBastion"
/>
# Create an Azure service health alert
---
{
  "recommendationOfferingId": "33537dde-bed2-4c9d-9bc3-0d92db2593a8",
  "recommendationOfferingName": "Azure Bastion",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "17ebccd8-1405-405c-8695-1981d115ffdc",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hybridnetworking.kusto.windows.net').database('aznwmds').f_Bastion_BastionHostsNeedingRecreation",
    "dataSource": "Kusto",
    "refreshInterval": "00.01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/bastionhosts",
  "recommendationFriendlyName": "RecreateBastionResource",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "bastionpm@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Cloudnet",
      "team": "Azure Bastion"
    },
    "serviceTreeId": "33537dde-bed2-4c9d-9bc3-0d92db2593a8"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1,
  "learnMoreLink": "https://docs.microsoft.com/azure/bastion/tutorial-create-host-portal",
  "description": "Delete and recreate your Azure Bastion resource before February 19, 2021",
  "longDescription": "We are unable to update your Azure Bastion resource due to its current configuration. Please delete and recreate your resource before February 19, 2021 to receive the updates. If you do not delete and recreate your resource by this date, it will automatically be deleted and recreated for you.",
  "potentialBenefits": "Receive necessary updates for your Azure Bastion resource.",
  "actions": [
    {
      "actionId": "fc52f841-6ebf-4f45-b5ec-668259bd45a5",
      "description": "Delete and recreate your Azure Bastion resource",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/bastion/tutorial-create-host-portal"
    }
  ],
  "displayLabel": "Delete and recreate your Azure Bastion resource before February 19, 2021",
  "additionalColumns": []
}
---