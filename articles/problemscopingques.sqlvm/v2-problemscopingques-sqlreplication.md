<properties 
  pageTitle="SQL Replication"
  description="SQL Replication"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740093"
  productPesIds="14745,16342"
  cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
  schemaVersion="1"
  articleId="61a28e3a-58dd-4d51-ba79-7dd074d2b2c1"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Replication
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Replication",
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
            "displayLabel": "What kind of SQL Server replication are you using?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Transactional",
                    "value": "Transactional"
                },
                {
                    "text": "Merge",
                    "value": "Merge"
                },
                {
                    "text": "Peer to Peer",
                    "value": "PeerToPeer"
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
