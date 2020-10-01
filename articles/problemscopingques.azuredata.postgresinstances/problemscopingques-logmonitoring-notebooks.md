<properties
	pageTitle="Troubleshoot using Notebooks"
	description="Troubleshoot using Notebooks"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747931"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="22296b9c-1faf-4703-b94b-67b267e1ea7a"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Troubleshoot using Notebooks
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Troubleshoot using Notebooks",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "notebook_problem",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Which Notebook do you have problem with?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Notebook provided by Microsoft",
					"text": "Notebook provided by Microsoft"
				}, {
					"value": "A Notebook you created",
					"text": "A Notebook you created"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "issue_outside_notebook",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Does the problem also happen if you run the failing command outside of the Notebook?",
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
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
