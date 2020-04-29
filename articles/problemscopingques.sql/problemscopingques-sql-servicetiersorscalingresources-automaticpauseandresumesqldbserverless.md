<properties
	articleId="problemscopingques-sql-servicetiersorscalingresources-automaticpauseandresumesqldbserverless"
	pageTitle="SQL Database"
	description="Scoping questions to capture issues with purchasing models"
	authors="andikshi"
	authoralias="andikshi"
	ms.author="andikshi"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32639119"
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
            "id": "issue_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What type of issue are you facing with serverless?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "configuring",
                    "text": "Creating a new database in serverless service tier?"
                },
                {
                    "value": "re-configuring",
                    "text": "Moving database from serverless compute tier into provisioned compute tier?"
                },
                {
                    "value": "existing_issues",
                    "text": "Issues with pause and resume of serverless database?"
                },
		{
                    "value": "Biling",
                    "text": "Isues with billing?"
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
            "id": "problem_start_time",
            "order": 6,
            "controltype": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Specify when the problem started",
            "infoBalloonText": "Specify when the problem started",
            "required": true,
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
