<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
    ms.author="aasdev"
    articleId="5152c401-2d14-4860-b59c-5c0ddc18e9f8_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,ussec,usnat"
    ownershipId="AzureAttestation_Attestation"
/>
# Attestation SDK Version Recommendation
---
{
   "recommendationOfferingId":"ed0474ab-5023-4fb4-ac86-05170f7c63ca",
   "recommendationOfferingName":"Microsoft Azure Attestation",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"3629448e-9b3e-4c5d-96ec-4760bbfde5ab",
   "dataSourceMetadata":{
      "streamNamespace":"cluster('https://azureslam.kusto.windows.net').database('AzureAttestationProd').GetAzureAdvisorRecommendedSdkReport",
      "dataSource":"Kusto",
      "refreshInterval":"1.00:00:00"
   },
   "recommendationCategory":"Performance",
   "recommendationImpact":"Medium",
   "recommendationResourceType":"Microsoft.Attestation/attestationProviders",
   "recommendationFriendlyName":"UpgradeAttestationSDK",
   "recommendationMetadataState":"Active",
   "owner":{
      "email":"aasdev@microsoft.com",
      "icm":{
         "routingId":"MDM://AzureAttestationService",
         "service":"Azure Security Engineering",
         "team":"Azure Attestation Service"
      },
      "serviceTreeId":"4377f503-9a93-4584-b6bb-d75c33b8bbd2"
   },
   "ingestionClientIdentities":[],
   "version":1,
   "learnMoreLink":"https://docs.microsoft.com/rest/api/attestation",
   "description":"Update Attestation SDK Version",
   "longDescription":"We have identified API calls from outdated Attestation SDKs for resources under this subscription. We recommend switching to the latest Attestation SDK versions. You need to update your existing code to use the latest SDK version. This ensures you receive the latest features and performance improvements.",
   "potentialBenefits":"Latest Attestation SDK contain fixes for known issues and additional improvements.",
   "supportedSDKLanguages":[".Net"],
   "actions":[{
         "actionId":"4578680a-f6fe-4215-9ebf-d71934f924fb",
         "description":"Learn how to update your Attestation SDK",
         "actionType":"Document",
         "documentLink":"{recommendedActionLearnMore}"
      },
      {
         "actionId":"38f0bbec-bfc8-47a4-a76f-9fbb385cc24f",
         "description":"View {version} release notes",
         "actionType":"Document",
         "documentLink":"{releaseNotes}"
      }
   ],
   "resourceMetadata":{
      "action":{
         "actionId":"1fb5de62-ffe1-44ab-9b6f-8762d808c381",
         "actionType":"Blade",
         "extensionName":"Microsoft_Azure_Attestation",
         "bladeName":"AttestationBlade",
         "metadata":{
            "id":"{resourceId}"
         },
         "documentLink":""
      }
   },
   "displayLabel":"Update Attestation SDK",
   "additionalColumns":[
      {
         "name":"language",
         "title":"SDK Language"
      },
      {
         "name":"version",
         "title":"Minimum Recommended Version"
      }
   ],
   "tip":"",
   "testData":"a724c543-53ce-44a6-b633-e11ef27839b7,/subscriptions/a724c543-53ce-44a6-b633-e11ef27839b7/resourceGroups/AASRunnerRG/providers/Microsoft.Attestation/attestationProviders/cacupdt2yngl3x5mcr0g
a724c543-53ce-44a6-b633-e11ef27839b7,/subscriptions/a724c543-53ce-44a6-b633-e11ef27839b7/resourceGroups/AASRunnerRG/providers/Microsoft.Attestation/attestationProviders/caegvtql3x5mcr0g1segg"
}
---
