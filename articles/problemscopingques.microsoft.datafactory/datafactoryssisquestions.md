<properties
	pageTitle="Scoping questions for DataFactory Azure SSIS issues"
	description="Scoping questions for DataFactory Azure SSIS issues"
	authors="arthurw"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32589777,32592906,32592904,32592905"
	productPesIds="15613"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Data Factory Azure SSIS Information
---
{
	"resourceRequired": true,
	"title": "Data Factory Azure SSIS Information",
	"fileAttachmentHint": "Please attach any relevant screen shots, logs, or JSON files",
	"formElements": [
		 {
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		  },
		  {
			"id": "region",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the region of the SSIS IR?",
			"required": false
		},
		{
			"id": "ir_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What is the name of the SSIS IR?",
			"required": true
		},
		{
			"id": "using_vnet",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Is this SSIS IR using a VNET?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
					"value": "true",
					"text": "Yes"
				},
				{
					"value": "false",
					"text": "No"
				},
				{
					"value": "unknown",
					"text": "I don't know"
				}
			],
			"required": false
		},
		{
			"id": "using_sql_managed_instance",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Is this SSIS IR using a SQL Managed Instance?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
					"value": "true",
					"text": "Yes"
				},
				{
					"value": "false",
					"text": "No"
				},
				{
					"value": "unknown",
					"text": "I don't know"
				}
			],
			"required": false
		},
		{
			"id": "problem_description",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details about the issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "More information on the exact issue."
				},{
					"text": "Error code, message, requestId, timestamp (if available)"
				}
			]
		}
	]	
}
---
