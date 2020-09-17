<properties
	pageTitle="Resize Storage volume used for the Data or the backups"
	description="Resize Storage volume used for the Data or the backups"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747927"
	productPesIds="17124"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="a2fe1f54-cd0c-479c-b50b-288297090e11"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Resize Storage volume used for the Data or the backups
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Resize Storage volume used for the Data or the backups",
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
			"id": "error_happening",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Was the error transient or is it still happening?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Transient Error",
					"text": "Transient Error"
				}, {
					"value": "Issue still happening",
					"text": "Issue still happening"
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
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
