<properties
	articleId="problemscopingques-sqldb-error-connecting-10928"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues for error 10928"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749513"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "SQL Database",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
         {
            "id": "is_reproducible",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Is the problem reproducible?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes, we can reproduce the problem consistently"
                },
                {
                    "value": "no",
                    "text": "No. The problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "error_text_10928",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the 10928 error text if available",
            "watermarkText": "Enter error text.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.  If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
