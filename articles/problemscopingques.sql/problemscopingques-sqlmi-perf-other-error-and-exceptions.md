<properties
	articleId="problemscopingques-sqldb-perf-other-error-and-exceptions"
	pageTitle="Azure SQL Database"
	description="Scoping questions to capture issues related to Other Errors and Exceptions"
	authors="Akio Hose"
	authoralias="akiohose"
	ms.author="akiohose"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748871"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "SQL Database Managed Instance",
    "fileAttachmentHint": "",
	"diagnosticCard": {
    "title": "Other errors Troubleshooter",
    "description": "Our Errors Troubleshooter can help you troubleshoot and solve your issue.",
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
                "text":"Query Store and Related Issues",
                "value": "Query_Store_and_Related_Issues"
            },
            {
                "text": "Issues with Bulk Insert",
                "value": "Issues_with_Bulk_Insert"
            },
            {
                "text": "Temp DB Full or other Issues with TempDB",
                "value": "Temp_DB_Full_or_other_Issues_with_TempDB"
            },
            {
                "text": "Error 9002: The transaction log for database X is full",
                "value": "Error_9002_The_transaction_log_for_database_X_is_full"
            },
            {
                "text": "None of the above",
                "value": "dont_know_answer"
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
            "displayLabel": "If applicable, provide the error text including the stack trace as well.",
            "watermarkText": "Error text or stack trace if available",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.  If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
