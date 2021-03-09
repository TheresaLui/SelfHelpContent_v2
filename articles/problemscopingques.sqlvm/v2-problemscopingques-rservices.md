<properties 
  pageTitle="R Services"
  description="R Services"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32788719"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="9341cf62-e518-4187-885d-224a35c4c829"
  ownershipId="AzureData_AzureSQLVM"
/>
# R Services
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "R Services",
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
            "id": "whatKind",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What kind of issue are you facing?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Need help setting up R Services",
                    "value": "setup"
                },
                {
                    "text": "Issue with Launchpad Service",
                    "value": "launchpad"
                },
                {
                    "text": "Issue with running R Scripts",
                    "value": "scripts"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I'm not sure/don't know"
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
