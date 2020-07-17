<properties
	articleId="problemscopingques-sqlmi-backup-restore-bc-restore-dropped-instance"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to get more details about restore dropped instance"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637302"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": false,
  "subscriptionRequired": false,
  "title": "Restore dropped instance",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When was the instance dropped?",
      "required": true
    },
    {
      "id": "mi_name",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "What is the name of the dropped Managed Instance?",
      "required": true
    },
    {
      "id": "mi_recreated",
      "order": 20,
      "controlType": "dropdown",
      "displayLabel": "Have you created a new MI with the same name? If not, please don’t do it. ",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the migration source",
			"dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
      "id": "recover_all_db",
      "order": 30,
      "controlType": "dropdown",
      "displayLabel": "Do you want to recover all the DBs?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the migration source",
			"dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
      "id": "recover_all_db",
      "order": 40,
      "controlType": "dropdown",
      "displayLabel": "If it’s not possible to recover a DB do you want to continue and exclude that DB?",
      "visibility": "recover_all_db == yes",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the migration source",
			"dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
      "id": "list_db_recover",
      "order": 50,
      "controlType": "multilinetextbox",
      "visibility": "recover_all_db == yes",
      "displayLabel": "What are the DBs you want to recover?",
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
