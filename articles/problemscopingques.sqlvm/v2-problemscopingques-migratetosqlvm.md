<properties 
  pageTitle="Migrate to SQL VM"
  description="Migrate to SQL VM"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740085"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="522f1914-feb4-4da7-b0ac-649582f71a7b"
  ownershipId="AzureData_AzureSQLVM"
/>
# Migrate to SQL VM
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Migrate to SQL VM",
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
            "id": "WhereToWhere",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Where are you planning to migrate from?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "On-premise VM",
                    "value": "OnPrem"
                },
                {
                    "text": "From another Azure VM",
                    "value": "AnotherVM"
                },
                {
                    "text": "Setting up hybrid environment",
                    "value": "HybridVM"
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
             "id": "How_Migrate",
             "visibility": null,
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "How are you planning to migrate the VM?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "Using Generalization/VHD",
                     "value": "GeneralizeVM"
                 },
                 {
                     "text": "Using ASR",
                     "value": "UsingASR"
                 },
                 {
                     "text": "By creating a new VM",
                     "value": "NewVM"
                 },
                 {
                     "text": "I'm not sure/Need guidance on same",
                     "value": "dont_know_answer_guidance"
                 }
             ],
             "dynamicDropdownOptions": null,
             "required": false,
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
