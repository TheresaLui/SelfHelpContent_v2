<properties
	articleId="problemscopingques-sqlmi-perf-timeouts"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture managed instance issues with timeouts in performance"
	authors="vitomaz-msft,MladjoA"
	authoralias="vitomaz"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637296"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "SQL Database Managed Instance",
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
            "id": "database_name",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What database is having issues?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "{resourceid}/databases?api-version=2017-03-01-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of databases",
                    "text": "Unable to get the list of databases"
                }
            ],
            "required": false
        },
        {
            "id": "problem_details",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": false,
            "displayLabel": "Specific Query Store query_id, plan hash, query hash or query text.",
            "watermarkText": "",
            "required": true
        },
        {
            "id": "impact",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is every execution of the query impacted?",
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
            ],
            "required": true
        },
        {
            "id": "latest_occurrence",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Latest occurrence of the issue timestamp (in UTC preferably)",
            "required": false
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