<properties
	pageTitle="Unexpected increase in resource consumption (CPU, Memory, I-O)"
	description="Unexpected increase in resource consumption (CPU, Memory, I-O)"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747934"
	productPesIds="17124"
	cloudEnvironments="Public"
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
			"id": "reproducible",
			"order": 2,
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
			"id": "arcenvironment",
			"order": 3,
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
			"id": "readwrite",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Is the workload load that is impacted more around reads or writes or both?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Mostly read",
					"text": "Mostly read"
				}, {
					"value": "Mostly write",
					"text": "Mostly write"
				}, {
					"value": "Both read and write",
					"text": "Both read and write"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "specific_query",
			"order": 5,
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
			"required": false
		}, {
			"id": "workload_increase",
			"order": 6,
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
			"required": false
		}, {
			"id": "servergroup_config",
			"order": 7,
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
			"id": "modify_indexes",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "Did you modify the indexes on your tables or reindexed the data?",
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
			"id": "add_workload",
			"order": 9,
			"controlType": "dropdown",
			"displayLabel": "Did you add any workload to your Kubernetes cluster outside of your Azure Arc setup?",
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
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
