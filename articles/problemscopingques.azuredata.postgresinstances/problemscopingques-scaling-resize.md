<properties
	pageTitle="Resize Storage volume used for the Data or the backups"
	description="Resize Storage volume used for the Data or the backups"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747927"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
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
			"id": "what_scale",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "What are you trying to scale?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Min vCore",
					"text": "Min vCore"
				}, {
					"value": "Max vCore",
					"text": "Max vCore"
				}, {
					"value": "Min memory",
					"text": "Min memory"
				}, {
					"value": "Max Memory",
					"text": "Max Memory"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "scale_up_down",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Are you trying to scale up or down?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Up",
					"text": "Up"
				}, {
					"value": "Down",
					"text": "Down"
				}, {
					"value": "Both",
					"text": "Both"
				}
			],
			"required": false
		}, {
			"id": "resources",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "If you are trying to scale up, are there enough resources in your Kubernetes cluster for your desired configuration?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
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
