<properties
	pageTitle="SQL Server - Azure Arc"
	description="SQL Server - Azure Arc"
	ms.author="amigan,ujpat,amamun"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748831,32748833"
	productPesIds="17126"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="db1317ea-ab6c-435d-b0a1-963f5a2e366c"
	ownershipId="AzureData_SQL_Server_Azure_Arc"
/>
# SQL Server - Azure Arc
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "SQL Server - Azure Arc",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "arc_configuration",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Have you already installed Microsoft Monitoring Agent?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description"
				}, {
					"text": "Provide additional information about your issue"
				}
			]
		}
	]
}
---
