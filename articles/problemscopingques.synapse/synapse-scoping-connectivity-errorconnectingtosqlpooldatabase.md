<properties
	schemaVersion = "1"
	selfHelpType = "problemScopingQuestions"
	cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	productPesIds = "15818"
	supportTopicIds = "32738770"
	pageTitle = "Connectivity/Error connecting to SQL pool database"
	description = "Connectivity/Error connecting to SQL pool database"
	articleId = "synapse-scoping-connectivity-errorconnectingtosqlpooldatabase"
	authors = "saltug"
	ms.author = "saltug"
/>

# Connectivity/Error connecting to SQL pool database

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Error connecting to SQL pool database",
    "diagnosticCard": {
        "title": "Connectivity Troubleshooter",
        "description": "The Connectivity Troubleshooter can identify the cause of many common service-related connection errors.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "dw_2",
            "order": 3,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
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
