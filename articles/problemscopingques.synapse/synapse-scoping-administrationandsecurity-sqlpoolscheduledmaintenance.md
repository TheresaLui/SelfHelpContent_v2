<properties
	schemaVersion = "1"
	selfHelpType = "problemScopingQuestions"
	cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	productPesIds = "15818"
	supportTopicIds = "32738823"
	pageTitle = "Administration and Security/SQL pool Scheduled Maintenance"
	description = "Administration and Security/SQL pool Scheduled Maintenance"
	articleId = "synapse-scoping-administrationandsecurity-sqlpoolscheduledmaintenance"
	authors = "saltug"
	ms.author = "saltug"
/>

# Administration and Security/SQL pool Scheduled Maintenance

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "SQL pool Scheduled Maintenance",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "required": true,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "infoBalloonText": ""
        },
        {
            "id": "dw_2",
            "order": 2,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What is the performance tier of the data warehouse at the time of the maintenance event?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "dw_3",
            "order": 3,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What is the region of your data warehouse?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "problem_description",
            "order": 4,
            "required": true,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "infoBalloonText": "",
            "useAsAdditionalDetails": true
        }
    ]
}
---

