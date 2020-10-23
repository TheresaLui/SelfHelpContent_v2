<properties
	pageTitle="Database Administration - Server Parameters"
	description="Database Administration - Server Parameters"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747918"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="3ffa140e-bee8-4335-b03f-c1504ede1b46"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Database Administration - Server Parameters
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Database Administration - Server Parameters",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "error_message",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "If an error was displayed, what was the error message?",
            "required": false
		}, {
			"id": "posgres_version",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What is the Postgres version of your server group?",
            "required": false
		}, {
			"id": "parameters",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What parameter(s) are your trying to change?",
            "required": false
		}, {
			"id": "tool",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Which tool did you use to change the server parameters?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Azdata",
					"text": "Azdata"
				}, {
					"value": "kubectl",
					"text": "kubectl"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "command_execute",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "What command are you trying to execute?",
            "required": false
		}, {
			"id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
