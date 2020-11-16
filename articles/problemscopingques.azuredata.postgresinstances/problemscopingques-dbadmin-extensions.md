<properties
	pageTitle="Database Administration - Issues or Questions related to Extensions"
	description="Database Administration - Issues or Questions related to Extensions"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747906"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="559da2d9-570d-4e03-9f66-7e478a09bb13"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Database Administration - Issues or Questions related to Extensions
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Database Administration - Issues or Questions related to Extensions",
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
			"id": "reproducible",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Is the problem reproducible or not?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Issue can be reproduced/Issue is live",
					"text": "Issue can be reproduced/Issue is live"
				}, {
					"value": "Issue is transient",
					"text": "Issue is transient"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "extension_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the name of the extension?",
            "required": false
		}, {
			"id": "readwrite",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What operation are you trying to do with the extension?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Preload",
					"text": "Preload"
				}, {
					"value": "Enable",
					"text": "Enable"
				}, {
					"value": "Create",
					"text": "Create"
				}, {
					"value": "Use",
					"text": "Use"
				}, {
					"value": "Others",
					"text": "Others"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
