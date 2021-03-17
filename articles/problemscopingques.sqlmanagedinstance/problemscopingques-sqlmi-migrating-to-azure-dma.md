<properties
	articleId="problemscopingques-sqlmi-migrating-to-azure-dma"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to capture dma issues"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32637252"
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
  "title": "Data Migration Assistant (DMA)",
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
      "id": "dma_version",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What version of DMA is being used?",
      "required": true
    },
    {
      "id": "project_type",
      "order": 20,
      "controlType": "dropdown",
      "displayLabel": "What is the project type causing the issue?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the project type where you are facing the issue",
			"dropdownOptions": [
                {
                    "value": "assessment",
                    "text": "Assessment"
                },
                {
                    "value": "migration",
                    "text": "Migration"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": true
    },
    {
      "id": "assessment_type",
      "order": 25,
      "controlType": "dropdown",
      "visibility": "project_type == assessment",
      "displayLabel": "What is the assessment type causing the issue?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the assessment type where you are facing the issue",
			"dropdownOptions": [
                {
                    "value": "db_engine",
                    "text": "Database Engine"
                },
                {
                    "value": "IS",
                    "text": "Integration Services"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": false
    },
    {
      "id": "db_source",
      "order": 30,
      "controlType": "dropdown",
      "displayLabel": "What is the SQL Server version from the source?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the SQL Server version",
			"dropdownOptions": [
                {
                    "value": "2005",
                    "text": "SQL Server 2005"
                },
                {
                    "value": "2008",
                    "text": "SQL Server 2008"
                },
                {
                    "value": "2008R2",
                    "text": "SQL Server 2008 R2"
                },
                {
                    "value": "2012",
                    "text": "SQL Server 2012"
                },
                {
                    "value": "2014",
                    "text": "SQL Server 2014"
                },
                {
                    "value": "2016",
                    "text": "SQL Server 2016"
                },
                {
                    "value": "2017",
                    "text": "SQL Server 2017"
                },
                {
                    "value": "aws",
                    "text": "AWS RDS for SQL Server"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": false
    },
    {
      "id": "migration_scope",
      "order": 35,
      "controlType": "dropdown",
      "visibility": "project_type == migration",
      "displayLabel": "What is the scope of the migration?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Choose the migration scope",
			"dropdownOptions": [
                {
                    "value": "schema_data",
                    "text": "Schema and Data"
                },
                {
                    "value": "schema",
                    "text": "Schema only"
                },
                {
                    "value": "data",
                    "text": "Data only"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
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
