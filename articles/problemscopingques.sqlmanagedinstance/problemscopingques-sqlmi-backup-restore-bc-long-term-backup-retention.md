<properties
	articleId="problemscopingques-sqlmi-backup-restore-bc-long-term-backup-retention"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to get more details about Long-term backup retention"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637272"
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
  "title": "Long-term backup retention",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did you face the issue?",
      "required": true
    },
    {
      "id": "type_issue",
      "order": 10,
      "controlType": "dropdown",
      "displayLabel": "What type of issue are you facing",
      "watermarkText": "Choose an option",
			"dropdownOptions": [
                {
                    "value": "config",
                    "text": "Creation or Configuration"
                },
                {
                    "value": "view",
                    "text": "View information"
                },
                {
                    "value": "delete",
                    "text": "Delete backups"
                },
                {
                    "value": "questions",
                    "text": "Questions about the Long-term Retention"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
            "id": "database_name",
            "order": 20,
            "controlType": "dropdown",
	    "visibility": "type_issue != questions || type_issue != dont_know_answer",
            "displayLabel": "What database are you configuring Long-Term Retention?",
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
      "id": "retention_plan",
      "order": 30,
      "controlType": "textbox",
      "visibility": "type_issue != questions || type_issue != dont_know_answer",
      "displayLabel": "What is the retention plan configuration?",
      "required": false
    },
    {
      "id": "list_db_recover",
      "order": 40,
      "controlType": "multilinetextbox",
      "visibility": "type_issue != questions || type_issue != dont_know_answer",
      "displayLabel": "What are the permissions of the user facing the issue?",
      "watermarkText": "Please provide the scope of the permissions, Subscription or Resource Group",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 99,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering",
      "required": true
    }
  ]
}
---
