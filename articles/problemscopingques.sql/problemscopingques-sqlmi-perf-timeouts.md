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
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "latest_occurrence",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Latest occurrence of the issue?",
            "required": true
        },
        {
            "id": "frequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Can you reproduce this performance issue consistently?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "consistently",
                    "text": "Yes, consistently"
                },
                {
                    "value": "randomly",
                    "text": "No, randomly"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "database_name",
            "order": 20,
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
            "id": "other_databases",
            "order": 21,
            "controlType": "dropdown",
            "displayLabel": "Is the same problem experienced on other databases?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "other_databases_yes",
                    "text": "Yes"
                },
                {
                    "value": "other_databases_no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "comparison",
            "order": 22,
            "controlType": "dropdown",
            "displayLabel": "What is your point of comparison?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "slower_than_before",
                    "text": "It is slower than it typically is"
                },
                {
                    "value": "slower_than_other_azure",
                    "text": "It is slower than another database server on Azure"
                },
                {
                    "value": "slower_from_vnet",
                    "text": "It is slower when connection is from VNET"
                },
                {
                    "value": "slower_from_non_azure",
                    "text": "It is slower than server on Non-Azure cloud Environment"
                },
                {
                    "value": "slower_from_onprem",
                    "text": "It is slower than database server running on VM/Locally"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "query_hash",
            "order": 30,
            "controlType": "textbox",
            "useAsAdditionalDetails": false,
            "displayLabel": "Do you know the Query Hash of the affected query(s)?",
            "watermarkText": "",
            "required": false
        },
	{
			"id": "recently_migrated",
			"order": 40,
			"controlType": "dropdown",
			"displayLabel": "Have you recently migrated to Azure?",
			"required": true,
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
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
		}, {
			"id": "application_type",
			"order": 43,
			"controlType": "dropdown",
			"displayLabel": "What is the application type? ",
			"visibility": "recently_migrated == Yes",
			"required": true,
			"dropdownOptions": [
				{
					"value": "morden_platform",
					"text": "Modern distributed platform (Ex: .Net, Java, Python, Ruby etc.)"
				},
				{
					"value": "legacy",
					"text": "Legacy (Ex: COBOL, PL-I, Assembler etc.)"
				},
				{
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
		}, {
			"id": "migration_backend",
			"order": 47,
			"controlType": "dropdown",
			"displayLabel": "What was the Pre-Migration backend ?  ",
			"visibility": "recently_migrated == Yes",
			"required": true,
			"dropdownOptions": [
				{
					"value": "sql_server",
					"text": "SQL Server"
				},
				{
					"value": "oracle",
					"text": "Oracle"
				},
				{
					"value": "db2",
					"text": "DB2"
				},
				{
					"text": "Other, don't know or not applicable",
					"value": "dont_know_answer"
				}
			]
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
