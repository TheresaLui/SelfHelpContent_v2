<properties 
  pageTitle="Storage Latency"
  description="Storage Latency"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740104"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="f0fae337-9699-4bc0-aa51-cc16e08da7fd"
 ownershipId="AzureData_AzureSQLVM"
/>
# Storage Latency
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Storage Latency",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "whichStorage",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What storage tier is being used for your data and transaction log files?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Standard Storage",
                    "value": "StandardStorage"
                },
                {
                    "text": "Premium Storage",
                    "value": "PremiumStorage"
                },
                {
                    "text": "Ultra SSD Storage",
                    "value": "UltraSSD"
                },
                {
                    "text": "I'm not sure/don't know",
                    "value": "dont_know_answer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
