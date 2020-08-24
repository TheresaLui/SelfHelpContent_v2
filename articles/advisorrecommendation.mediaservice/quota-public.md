<properties
    pageTitle="Azure Media Services quotas and limits."
    description="Azure Media Services quotas and limits."
    author="zimao"
    ms.author="zimao,amscis"
    articleId="b7c9fd99-a979-40b4-ab48-b1dfab6bb41a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
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
    "streamNamespace": "cluster('https://mediaservicestest.kusto.windows.net').database('MediaServicesTest').QuotaRecommendation",
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
  "version": 1.1,
  "learnMoreLink": "https://aka.ms/ams-quota-recommendation/",
  "description": "Increase the quota limits in your media account.",
  "longDescription": "You may ask for the quotas to be raised, by opening a support ticket. Include detailed information in the request on the desired quota changes, use-case scenarios, media account name and regions required. Do not create additional Azure Media Services accounts in an attempt to obtain higher limits.",
  "potentialBenefits": "Avoid any disruption to service due to customer exceeding quota limits.",
  "actions": [
    {
      "actionId": "fbc706f9-98a1-444a-8370-0fb7e121a80c",
      "description": "Opening a support ticket.",
      "actionType": "Document",
      "documentLink": "https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7df7d122-7954-482a-a658-cc9574e9dd1a",
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