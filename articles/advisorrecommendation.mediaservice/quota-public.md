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
  "recommendationImpact": "Low",
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
  "version": 1.0,
  "learnMoreLink": "https://azure.microsoft.com/services/media-services/",
  "description": "Increase the quota limitation in your media account.",
  "longDescription": "You may ask for the quotas to be raised, by opening a support ticket. Include detailed information in the request on the desired quota changes, use-case scenarios, and regions required. Do not create additional Azure Media Services accounts in an attempt to obtain higher limits.",
  "potentialBenefits": "TODO HERE",
  "actions": [
    {
      "actionId": "fbc706f9-98a1-444a-8370-0fb7e121a80c",
      "description": "Read more about account resouce quotas and limits",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/media-services/latest/limits-quotas-constraints"
    }
  ],
  "displayLabel": "Increase Media Account Quota Limitation",
  "tip": "",
  "costSavingInfo": "",
  "additionalColumns" :["{ \"name\": \"quotaType\", \"title\": \"Quota Limit Type\"}"],
  "testData": "628bddd1-d701-4273-8a5c-6ae0bd476c83,/subscriptions/628bddd1-d701-4273-8a5c-6ae0bd476c83/resourceGroups/zimao1/providers/microsoft.media/mediaservices/zimao1111,\"{\"\"quotaType\"\":\"\"TEST\"\"}\""
}
---