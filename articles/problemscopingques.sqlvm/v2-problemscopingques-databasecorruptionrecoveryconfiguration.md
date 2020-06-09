<properties 
  pageTitle="Database corruption, recovery, configuration"
  description="Database corruption, recovery, configuration"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740077"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="7c03a334-00bf-4595-b0b6-af685e10d24f"
  ownershipId="AzureData_AzureSQLVM"
/>
# Database corruption, recovery, configuration
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database corruption, recovery, configuration",
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
                    "text": "Database in corrupted/suspect state",
                    "value": "DBCorrupted"
                },
                {
                    "text": "Database in recovery pending state",
                    "value": "DBRecovery"
                },
                {
                    "text": "Configure database settings/Best Practices",
                    "value": "DBConfiguration"
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
             "id": "whichChecks",
             "visibility": "whichArea == DBCorrupted",
             "order": 3,
             "controlType": "dropdown",
             "displayLabel": "Did you run the command 'dbcc checkdb' against the database?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "It completed with no errors",
                     "value": "NoError"
                 },
                 {
                     "text": "It reported errors",
                     "value": "Error"
                 },
                 {
                     "text": "I'm not sure/don't know",
                     "value": "dont_know_answer"
                 }
             ],
             "dynamicDropdownOptions": null,
             "required": false,
             "maxLength": 0,
             "useAsAdditionalDetails": false,
             "numberOfLines": 0
        },
        {
             "id": "WhenFound",
             "visibility": "whichArea == DBRecovery",
             "order": 4,
             "controlType": "dropdown",
             "displayLabel": "When did you first find out the database was in Recovery Pending?",
             "watermarkText": "Choose an option",
             "content": null,
             "infoBalloonText": null,
             "dropdownOptions": [
                 {
                     "text": "After SQL Service crashed",
                     "value": "SQLCrashed"
                 },
                 {
                     "text": "After applying patches",
                     "value": "ApplyingPatch"
                 },
                 {
                     "text": "After SQL service or database failover",
                     "value": "DBFailover"
                 },
                 {
                     "text": "I'm not sure/don't know",
                     "value": "dont_know_answer"
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
