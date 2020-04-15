<properties
	schemaVersion = "1"
	selfHelpType = "problemScopingQuestions"
	cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	productPesIds = "15818"
	supportTopicIds = "32738767"
	pageTitle = "SQL Performance and Query Execution/Data export using CETAS in SQL on-demand"
	description = "SQL Performance and Query Execution/Data export using CETAS in SQL on-demand"
	articleId = "synapse-scoping-sqlperformanceandqueryexecution-dataexportusingcetasinsqlon"
	authors = "saltug"
	ms.author = "fipopovi, saltug"
/>
# SQL Performance and Query Execution/Data export using CETAS in SQL on-demand
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Data export using CETAS in SQL on-demand",
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
            "watermarkText": "please include distributed statement id",
            "infoBalloonText": ""
        },
        {
            "id": "sqlod_3",
            "order": 3,
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
            "id": "sqlod_4",
            "order": 4,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "What storage account type do you want to query? (Blob Storage, ADLS Gen1, ADLS Gen2)",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions":
            [
                {
                    "value": "Blob Storage",
                    "text": "Blob Storage"
                },
                {
                    "value": "ADLS Gen1",
                    "text": "ADLS Gen1"
                },
                {
                    "value": "ADLS Gen2",
                    "text": "ADLS Gen2"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "sqlod_5",
            "order": 5,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "What type of credential do you use for SELECT part of CETAS query? (UserIdentity, ManagedIdentity, SAS)",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions":
            [
                {
                    "value": "UserIdentity",
                    "text": "UserIdentity"
                },
                {
                    "value": "ManagedIdentity",
                    "text": "ManagedIdentity"
                },
                {
                    "value": "SAS",
                    "text": "SAS"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "sqlod_6",
            "order": 6,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "What storage account type do you want to export data to? (Blob Storage, ADLS Gen1, ADLS Gen2)",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions":
            [
                {
                    "value": "Blob Storage",
                    "text": "Blob Storage"
                },
                {
                    "value": "ADLS Gen1",
                    "text": "ADLS Gen1"
                },
                {
                    "value": "ADLS Gen2",
                    "text": "ADLS Gen2"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "sqlod_7",
            "order": 7,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "What type of credential do you use for CET part of CETAS query? (UserIdentity, ManagedIdentity, SAS)",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions":
            [
                {
                    "value": "UserIdentity",
                    "text": "UserIdentity"
                },
                {
                    "value": "ManagedIdentity",
                    "text": "ManagedIdentity"
                },
                {
                    "value": "SAS",
                    "text": "SAS"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 8,
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

