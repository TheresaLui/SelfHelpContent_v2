<properties
    pageTitle="Azure Media Services quotas and limits."
    description="Azure Media Services quotas and limits."
    author="zimao"
    ms.author="zimao,amscis"
    articleId="b7c9fd99-a979-40b4-ab48-b1dfab6bb41a_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('https://mediaservicesfairfax.usgovvirginia.kusto.usgovcloudapi.net').database('mediaservicesfairfax').QuotaRecommendation",
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
  "learnMoreLink": "https://aka.ms/ams-quota-recommendation/",
  "description": "Increase Media Services quotas or limits to ensure continuity of service.",
  "longDescription": "Please be advised that your media account is about to hit its quota limits. Please review current usage of Assets, Content Key Policies and Stream Policies for the media account. To avoid any disruption of service, you should request quota limits to be increased for the entities that are closer to hitting quota limit. You can request quota limits to be increased by opening a ticket and adding relevant details to it. Please don't create additional Azure Media accounts in an attempt to obtain higher limits.",
  "potentialBenefits": "Avoid any disruption to service due to customer exceeding quota limits.",
  "actions": [
    {
      "actionId": "d33626ab-f35a-4777-a4fe-a7f38b2517da",
      "description": "Create a quota request.",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Support",
      "bladeName": "NewSupportRequestV3Blade",
      "metadata": {
            "subscriptionId": "{subscriptionId}",
            "issueType": "06bfd9d3-516b-d5c6-5802-169c800dec89",
            "topicId": "eb747862-5a4c-b6de-e173-02095d17fd4d"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "4933f3fd-d32f-415e-b37c-1cc69ac04fa7",
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
