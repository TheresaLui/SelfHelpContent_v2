<properties
	articleId="problemscopingques-sqlmi-backup-restore-bc-geo-restore"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to get more details about geo-restore issue"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637265"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Geo-Restore",
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
                    "value": "fail",
                    "text": "Command or request fail"
                },
                {
                    "value": "long",
                    "text": "Restore taking too long"
                },
                {
                    "value": "view",
                    "text": "Can't view available backups"
                },
                {
                    "value": "questions",
                    "text": "Questions about Geo-Restore"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer or issue not listed"
                }
            ],
            "required": true
    },
    {
            "id": "original_instance",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "What's the Managed Instance name where the backup was taken?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/managedInstances?api-version=2018-06-01-preview",
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
                    "value": "Unable to get the list of instances",
                    "text": "Unable to get the list of instances"
                }
            ],
            "required": false
    },
    {
            "id": "destination_instance",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "What's the Managed Instance name where you want to restore?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Sql/managedInstances?api-version=2018-06-01-preview",
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
                    "value": "Unable to get the list of instances",
                    "text": "Unable to get the list of instances"
                }
            ],
            "required": false
    },
    {
            "id": "db_restore",
            "order": 40,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the database(s) name(s) to be restored.",
            "required": false
    },
    {
            "id": "request_method",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "How is the restore being requestd?",
            "watermarkText": "Choose an option",
 			      "dropdownOptions": [
                {
                    "value": "portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "ps",
                    "text": "PowerShell"
                },
                {
                    "value": "cli",
                    "text": "CLI"
                },
                {
                    "value": "rest",
                    "text": "REST API"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
            "id": "version",
            "order": 60,
            "controlType": "textbox",
	          "visibility": "request_method == ps && request_method == cli && request_method == rest",
            "displayLabel": "What is the version number being used?",
            "required": false
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
