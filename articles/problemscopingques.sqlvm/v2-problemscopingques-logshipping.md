<properties 
  pageTitle="Log Shipping"
  description="Log Shipping"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740083"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="42711a95-fe3f-4620-9bfc-ec3092024abd"
  ownershipId="AzureData_AzureSQLVM"
/>
# Log Shipping
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Log Shipping",
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
            "displayLabel": "What kind of Log Shipping issue are you facing?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Job errors or alerts",
                    "value": "JobErrors"
                },
                {
                    "text": "Connectivity errors",
                    "value": "ConnectivityErrors"
                },
                {
                    "text": "Restore failures",
                    "value": "RestoreFailure"
                },
                {
                    "text": "Synchronization or Performance",
                    "value": "SyncOrPerf"
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
