<properties
	articleId="problemscopingques-sqlmi-migrating-to-azure-ssma"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture SSMA issues"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637309"
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
  "title": "SQL Server Migration Assistant (SSMA)",
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
      "id": "ssma_version",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "What version of SSMA is being used?",
      "required": true
    },
    {
      "id": "ssma_source",
      "order": 20,
      "controlType": "dropdown",
      "displayLabel": "What is the migration source?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the migration source",
			"dropdownOptions": [
                {
                    "value": "access",
                    "text": "Access"
                },
                {
                    "value": "db2",
                    "text": "DB2"
                },
                {
                    "value": "mysql",
                    "text": "MySQL"
                },
                {
                    "value": "oracle",
                    "text": "Oracle"
                },
                {
                    "value": "sap",
                    "text": "SAP ASE"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
      "id": "source_version",
      "order": 30,
      "controlType": "textbox",
      "displayLabel": "What is the source DB engine version being used?",
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
