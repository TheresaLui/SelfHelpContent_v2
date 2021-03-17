<properties
    pageTitle="Azure Media Services quotas and limits."
    description="Azure Media Services quotas and limits."
    author="zimao"
    ms.author="zimao,amscis"
    articleId="b7c9fd99-a979-40b4-ab48-b1dfab6bb41a_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="StorageMediaEdge_Media"
/>
# Sample title
---
{
  "recommendationOfferingId": "0d10d44d-cd3a-4aa7-81da-53038a753a94",
  "recommendationOfferingName": "Media Services",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b7c9fd99-a979-40b4-ab48-b1dfab6bb41a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://mediaservicesmooncake.chinaeast2.kusto.chinacloudapi.cn').database('mediaservicesmooncake').QuotaRecommendation",
    "dataSource": "Kusto",
    "refreshInterval": "1:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.media/mediaservices",
  "recommendationFriendlyName": "AccountQuotaLimit",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "amscis@microsoft.com",
    "icm": {
      "routingId": "AIMS://AMSPE",
      "service": "Media Services",
      "team": "2nd Tier: Common Platform"
    },
    "serviceTreeId": "44a2b1b8-0556-4403-8261-fe6a9172ea32"
  },
  "ingestionClientIdentities": [],
  "version": 1.3,
  "learnMoreLink": "https://aka.ms/ams-quota-recommendation-cn/",
  "description": "Increase Media Services quotas or limits to ensure continuity of service.",
  "longDescription": "Please be advised that your media account is about to hit its quota limits. Please review current usage of Assets, Content Key Policies and Stream Policies for the media account. To avoid any disruption of service, you should request quota limits to be increased for the entities that are closer to hitting quota limit. You can request quota limits to be increased by opening a ticket and adding relevant details to it. Please don't create additional Azure Media accounts in an attempt to obtain higher limits.",
  "potentialBenefits": "Avoid any disruption to service due to customer exceeding quota limits.",
  "actions": [
    {
      "actionId": "165b34a1-b7ec-478e-8062-25df1c0429ee",
      "description": "Create a quota request.",
      "actionType": "Document",
      "documentLink" : "https://support.azure.cn/support/support-azure/"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d2f21b61-b626-40cd-b517-df28bad6b519",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase Media Account Quota Limits",
  "tip": "",
  "costSavingInfo": "",
  "additionalColumns" :[{ "name": "quotaType", "title": "Quota Limit Type"}],
  "testData": "628bddd1-d701-4273-8a5c-6ae0bd476c83,/subscriptions/628bddd1-d701-4273-8a5c-6ae0bd476c83/resourceGroups/zimao1/providers/microsoft.media/mediaservices/zimao1111,\"{\"\"quotaType\"\":\"\"TEST\"\"}\""
}
---
