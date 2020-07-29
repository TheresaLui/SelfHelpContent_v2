<properties 
  pageTitle="Manage SQL VM Resource provider and features"
  description="Manage SQL VM Resource provider and features"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740084"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, Mooncake, USSEC, USNAT"
  schemaVersion="1"
  articleId="996f13c9-bc9e-4bdc-a477-52e83ddd8b3c"
  ownershipId="AzureData_AzureSQLVM"
/>
# Manage SQL VM Resource provider and features
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Manage SQL VM Resource provider and features",
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
            "id": "What_Feature",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What feature do you need help with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL VM Resource Provider setup or troubleshoot",
                    "value": "OnPrem"
                },
                {
                    "text": "Change Licensing to AHUB/Pay as you go",
                    "value": "AnotherVM"
                },
                {
                    "text": "Configure storage configuration",
                    "value": "HybridVM"
                },
                {
                    "text": "Configure Automated patching",
                    "value": "AnotherVM"
                },
                {
                    "text": "Configure Automated backup",
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
             "id": "What_Platform",
             "visibility": null,
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "What platform are you using to manage the selected feature?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "Azure Portal",
                     "value": "AzurePortal"
                 },
                 {
                     "text": "Azure PowerShell",
                     "value": "AzurePowerShell"
                 },
                 {
                     "text": "Azure CLI",
                     "value": "AzureCLI"
                 },
                 {
                     "text": "I'm not sure/don't know",
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
