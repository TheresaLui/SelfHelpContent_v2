<properties
	schemaVersion = "1"
	selfHelpType = "problemScopingQuestions"
	cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	productPesIds = "15818"
	supportTopicIds = "32738789"
	pageTitle = "How-To/Portal and Client Tools for SQL on-demand"
	description = "How-To/Portal and Client Tools for SQL on-demand"
	articleId = "synapse-scoping-howto-portalandclienttoolsforsqlondemand"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>
# How-To/Portal and Client Tools for SQL on-demand
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Portal and Client Tools for SQL on-demand",
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
            "id": "sqlod_2",
            "order": 2,
            "required": false,
            "controlType": "multilinetextbox",
            "displayLabel": "If an error was displayed, what was the error message (including distributed statement id, if any)?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "sqlod_3",
            "order": 3,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What tool and which version of tool do you use to connect?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "sqlod_4",
            "order": 4,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "Do you use AAD or SQL login?",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions":
            [
                {
                    "value": "Azure Active Directory",
                    "text": "Azure Active Directory"
                },
                {
                    "value": "SQL",
                    "text": "SQL"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 5,
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

