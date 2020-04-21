<properties
	articleId="problemscopingques-sql-createdropresources-elasticjoborjobagent"
	pageTitle="SQL Database"
	description="Scoping questions to capture CRUD issues for elastic jobs or agents"
	authors="andikshi"
	authoralias="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32739626"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
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
            "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What issue are you facing with elastic jobs?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "creation_agent",
                    "text": "Creating or configuring the elastic job agent?"
                },
                {
                    "value": "creation_jobs",
                    "text": "Creating running or managing jobs?"
                },
                {
                    "value": "jobs_performance",
                    "text": "Issues with elastic jobs performance?"
                },
		{
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "attempt_method",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What method are you using",
            "required": true,
	    "visibility": "issue_type == creation_agent",
            "dropdownOptions": [
                {
                    "value": "powershell",
                    "text": "Powershell"
                },
                {
                    "value": "TSQl",
                    "text": "TSQL"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "encountering_an_error",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you encountering an error message?",
	    "required": false,
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Unsure"
                }
            ]
        },
        {
            "id": "error_message",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error message",
            "required": false,
            "visibility": "encountering_an_error == Yes"
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
    ]
}
---
