<properties
	articleId="problemscopingques-sqldb-indexmaintenance-and-statistics"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related Index maintenance and Statistics"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749517"
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
                    "text": "Yes, the problem is reproducible."
                },
                {
                    "value": "no",
                    "text": "No, the problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "indexstat_maintenance",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "How frequent are the indexes and statistics maintained?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "daily",
                    "text": "Daily"
                },
                {
                    "value": "weekly",
                    "text": "Weekly"
                },
                {
                    "value": "monthly",
                    "text": "Monthly"
                },
                {
                    "value": "every_few_months",
                    "text": "Every few months"
                },
                {
                    "value": "not_maintained",
                    "text": "Not maintained"
                },
                {
                    "value": "other",
                    "text": "Other (Please describe in the text box below)"
                }
            ],
            "required": false
        },
          {
            "id" : "indexstat_maintenance_other",
            "order" : 31,
            "visibility" : "indexstat_maintenance == other",
            "controlType" : "textbox",
            "displayLabel" : "Please describe index/statistics maintenance frequency",
            "watermarkText" : "Describe other",
            "required": true
        },
         {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for index/statistics maintenance or issue observed",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.  If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
