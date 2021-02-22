<properties
	pageTitle="Add worker nodes to Hyperscale server group"
	description="Add worker nodes to Hyperscale server group"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747926"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="db3032f8-5810-4125-b37a-170ff122a007"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Add worker nodes to Hyperscale server group
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Add worker nodes to Hyperscale server group",
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
			"id": "command_used",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What command did you use?",
			"required": false
		}, {
			"id": "workernodes",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "What is the number of worker nodes you are trying to scale from?",
			"required": false
		}, {
			"id": "smallernode",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "Does the problem still occur if you add a smaller number of nodes as intermediate step?",
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
