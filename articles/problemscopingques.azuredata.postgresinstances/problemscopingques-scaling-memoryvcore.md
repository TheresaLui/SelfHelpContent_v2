<properties
	pageTitle="Scaling Memory Vcore for Hyperscale Server Group"
	description="Scaling Memory Vcore for Hyperscale Server Group"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747928"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="7d321539-451c-4ef0-94da-d2cc2343195a"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Scaling Memory Vcore for Hyperscale Server Group
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Scaling Memory Vcore for Hyperscale Server Group",
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
			"id": "scaleupdown",
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
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "resources",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "If you are trying to scale up, are there enough resources in Kubernetes cluster to accept desired configuration?",
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
			"required": false
		}, {
			"id": "command_used",
			"order": 7,
			"controlType": "textbox",
			"displayLabel": "What command did you use?",
			"required": true
		}, {
			"id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
