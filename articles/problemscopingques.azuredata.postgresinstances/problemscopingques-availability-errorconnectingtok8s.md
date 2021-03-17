<properties
	pageTitle="Error connecting to Kubernetes cluster (kubectl, azdata)"
	description="Error connecting to Kubernetes cluster (kubectl, azdata)"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747903"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6e2506b9-8c9e-4eb8-9515-cd592f8ab0e2"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Error connecting to Kubernetes cluster (kubectl, azdata)
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Error connecting to Kubernetes cluster (kubectl, azdata)",
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
			"id": "error_transient",
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
