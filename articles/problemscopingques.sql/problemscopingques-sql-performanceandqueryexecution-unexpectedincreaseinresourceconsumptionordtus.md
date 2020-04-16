<properties
	articleId="problemscopingques-sql-performanceandqueryexecution-unexpectedincreaseinresourceconsumptionordtus"
	pageTitle="SQL Database"
	description="Scoping questions for performance issue"
	authors="andikshi"
	authoralias="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32630459"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "title": "Database",
    "fileAttachmentHint": "",
    "subscriptionRequired": false,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controltype": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Specify when the problem started",
            "infoBalloonText": "Specify when the problem started",
            "required": true
        },
        {
            "id": "attempt_method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Was there any significant change in your environment\usage recently?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "workload",
                    "text": "My workload increased.
                },
                {
                    "value": "Service tier",
                    "text": "I changed my database service tier recently."
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        }
    ]
}
---
