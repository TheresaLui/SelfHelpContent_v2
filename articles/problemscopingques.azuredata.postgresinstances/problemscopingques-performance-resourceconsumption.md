<properties
	pageTitle="Unexpected increase in resource consumption (CPU, Memory, I-O)"
	description="Unexpected increase in resource consumption (CPU, Memory, I-O)"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747934"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="4131b906-2ae8-462e-b678-6267d1ae01c3"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Unexpected increase in resource consumption (CPU, Memory, I-O)
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Unexpected increase in resource consumption (CPU, Memory, I-O)",
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
			"displayLabel": "Is this performance issue happening only in an Azure Arc Environment?",
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
			"id": "specific_query",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Is the issue about a specific query or is more general?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Specific query or set of queries",
					"text": "Specific query or set of queries"
				}, {
					"value": "General Performance",
					"text": "General Performance"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "workload_increase",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Has your workload increased during this time?",
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
			"order": 5,
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
