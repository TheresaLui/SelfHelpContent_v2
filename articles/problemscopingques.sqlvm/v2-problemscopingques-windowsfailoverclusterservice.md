<properties 
  pageTitle="Windows Failover Cluster Service"
  description="Windows Failover Cluster Service"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740116"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="770d7885-eed5-40c6-9360-eb101bce2745"
  ownershipId="AzureData_AzureSQLVM"
/>
# Windows Failover Cluster Service
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Windows Failover Cluster Service",
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
            "id": "whichReplication",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation do you need assistance with?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Create a Windows Server Failover Cluster",
                    "value": "CreateWsfc"
                },
                {
                    "text": "Manage existing Windows Server Failover Cluster",
                    "value": "ManageExistingWsfc"
                },
                {
                    "text": "Troubleshoot cluster performance problems",
                    "value": "TroubleshootPerfWsfc"
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
