<properties 
  pageTitle="SQL agent, Jobs, Database mail"
  description="SQL agent, Jobs, Database mail"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740090"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="89a8d1b0-c5fe-4775-b6b8-52d692ad4995"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL agent, Jobs, Database mail
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL agent, Jobs, Database mail",
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
            "id": "whichArea",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What area do you need help with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "SQL Agent Job",
                    "value": "AgentJob"
                },
                {
                    "text": "Issues with Database Mail",
                    "value": "DBMail"
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
