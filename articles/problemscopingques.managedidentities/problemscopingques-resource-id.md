<properties
    pageTitle="Managed Identity Issue"
    description="Managed Identity Issue"
    ms.author="t-adade"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32690728,32690729,32690730"
    productPesIds="16985"
    articleId="problemscopingques-Problem retrieving token or assigning identity to resource"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    ownershipID="AzureIdentity_Managed Identities"
    schemaVersion="1"
/>

# Azure Managed Identity
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Problem acquiring tokens for the managed identity",
  "fileAttachmentHint": "",
  "formElements":[
  {
    "id": "problem_start_time",
    "order": 1,
    "controlType": "datetimepicker",
    "displayLabel": "When did the problem start?",
    "required": true
    },
    {
    "id": "ResourceID",
    "order": 2,
    "controlType": "textbox",
    "displayLabel": "Resoure ID",
    "watermarkText": "Provide Resource ID for Resource with issue",
    "required": true,
    "useAsAdditionalDetails": true
    }
    ,
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }]
}
---
