<properties
	pageTitle="SQL Server - Azure Arc"
	description="SQL Server - Azure Arc"
	ms.author="amigan,ujpat,amamun"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32748837,32748843,32748839,32748841"
	productPesIds="17126"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6d8e01f3-967c-4b95-950e-a69f36f1be03"
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
			"displayLabel": "Have you already configured Azure Arc Server Resource, before you can install SQL Arc resouce?",
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
			"id": "arc_registration",
			"order": 3,
			"visibility": "arc_configuration == Yes",
			"controlType": "multiselectdropdown",
			"displayLabel": "What difficulties are you facing with SQL Server Azure Arc Resource?",
			"dropdownOptions": [{
					"value": "script_fails",
					"text": "Registering SQL Arc resource with script fails"
				}, {
					"value": "cannot_see_instance",
					"text": "Cannot see registered SQL instance on Azure Portal"
				}, {
					"value": "more_info",
					"text": "I want to know more about the product"
				}
			],
			"required": false
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
