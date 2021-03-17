<properties
	pageTitle="Unexpected errors, Behaviours or exceptions while executing a query"
	description="Unexpected errors, Behaviours or exceptions while executing a query"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745094"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="9536a5f9-1662-4480-8534-09df3691034d"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Unexpected errors, Behaviours or exceptions while executing a query
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Unexpected errors, Behaviours or exceptions while executing a query",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "arcenvironment",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Is this issue happening only in an Azure Arc Environment?",
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
			"id": "servergroup_config",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Did you change the configuration of server group or your Kubernetes cluster recently/prior the problem started occurring?",
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
