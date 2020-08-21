<properties
pageTitle="Quota or limits increase"
description="Quota or limits increase"
service="microsoft.CognitiveServices"
resource="accounts"
authors="alexeyo26"
ms.author="alexeyo"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683855"
productPesIds="16870"
cloudEnvironments="public, MoonCake, fairfax"
articleId="Speech_Services_quotaOrSubsciptonIssues_quotaOrLimitsIncrease"
ownershipId="AzureCogSvc_CognitiveServices"
/>

# Quota or limits increase

If you receive many **Response Codes 429 ("Too many requests")** or you anticipate a **serious growth** of the workload review your Speech resource quotas and limits. Request adjustment if needed and applicable, and follow the described best practices to minimize issues related to throttling.

Jump to [Text-to-speech: Recommended Steps](#text-to-speech-recommended-steps)

## Speech-to-text: Recommended Steps

- Get familiar with [Speech-to-Text Quotas and Limits per Speech resource](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits#speech-to-text-quotas-and-limits-per-speech-resource)
  - Note, that only **Concurrent Request limit** parameter value for resources using **Standard (S0)** pricing tier can be adjusted
  - [Ensure you follow the best practices](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits#detailed-description-quota-adjustment-and-best-practices)
- If applicable [request the increase](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits#speech-to-text-increasing-online-transcription-concurrent-request-limit)

## Text-to-speech: Recommended Steps

- Get familiar with [Text-to-Speech Quotas and Limits per Speech resource](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits#text-to-speech-quotas-and-limits-per-speech-resource)
  - Note, that only **Concurrent Request limit** parameter value for resources using **Standard (S0)** pricing tier can be adjusted
  - [Ensure you follow the best practices](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits#detailed-description-quota-adjustment-and-best-practices)
- If applicable [request the increase](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits#text-to-speech-increasing-transcription-concurrent-request-limit-for-custom-voice)

## **Recommended Documents**

- [Speech Services Quotas and Limits](https://docs.microsoft.com/azure/cognitive-services/speech-service/speech-services-quotas-and-limits)