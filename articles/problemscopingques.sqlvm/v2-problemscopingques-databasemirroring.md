<properties 
  pageTitle="Database Mirroring"
  description="Database Mirroring"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740078"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="bd7cc2b7-c2e1-45bd-b493-333caa17bd3a"
  ownershipId="AzureData_AzureSQLVM"
/>
# Database Mirroring
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Mirroring",
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
            "displayLabel": "What kind of Database Mirroring issue are you facing?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Setting up Mirroring",
                    "value": "SetupMirroring"
                },
                {
                    "text": "Connectivity issues",
                    "value": "ConnectivityIssues"
                },
                {
                    "text": "Synchronization & Performance",
                    "value": "SyncAndPerformance"
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
