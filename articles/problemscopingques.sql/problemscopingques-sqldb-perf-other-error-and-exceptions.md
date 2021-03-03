<properties
	articleId="problemscopingques-sqldb-perf-other-error-and-exceptions"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to Other Errors and Exceptions"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32749519"
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
	"diagnosticCard": {
    "title": "Other errors Troubleshooter",
    "description": "Our other errors Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
 	{
            "id": "othererrorsandexception_issue_type",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Choose an option that best describes your issue.",
            "watermarkText": "Other Common Peformance Issues",
            "infoBalloonText": "Other common peformance issue categories",
            "dropdownOptions": [
            {
            "value":"Query Store and Related Issues",
            "text": "Query_Store"
            },
            {
            "value": "Issues with Bulk Insert",
            "text": "Bulk_Insert"
            },
             {
            "value": "Temp DB Full other Issues with TempDB",
            "text": "Temp_DB"
            },
             {
            "value": "Error 9002: The transaction log for database X is full",
            "text": "Transaction_Log_Full"
            },
            {
            "value": "dont_know_answer",
            "text": "None of the above"
            }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
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
                    "text": "No.  The problem occurs randomly"
                }
            ],
            "required": false
        },
        {
            "id": "observed_problem",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "If applicable, please provide the error text including the stack trace as well.",
            "watermarkText": "Error text or stack trace if available",
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
