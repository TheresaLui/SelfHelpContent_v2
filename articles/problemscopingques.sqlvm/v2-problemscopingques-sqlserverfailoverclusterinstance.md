<properties pageTitle="SQL Server Failover Clustered Instance"
  description="SQL Server Failover Clustered Instance"
  authors="ujpat,amamun"
         ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740097"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="4f2ee7cc-5f0e-40e6-ba9e-0f1993d57fac"
 ownershipId="AzureData_AzureSQLVM"
/>
# SQL Server Failover Clustered Instance
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Server Failover Clustered Instance",
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
            "id": "which_resource",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What area do you need assistance with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Configuring SQL FCI",
                    "value": "FCIConfiguration"
                },
                {
                    "text": "Manage or troubleshoot errors",
                    "value": "FCITroubleshooting"
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
