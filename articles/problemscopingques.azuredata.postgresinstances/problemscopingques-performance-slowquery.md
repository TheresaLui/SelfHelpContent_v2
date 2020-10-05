<properties
	pageTitle="Slow Query Performance or Time-outs"
	description="Slow Query Performance or Time-outs"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745092"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="a1f03bc9-1e4f-4622-9eee-683821117a6b"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Slow Query Performance or Time-outs
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Slow Query Performance or Time-outs",
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
			"required": true
		}, {
			"id": "connection_pooling",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Do you have connection pooling enabled?",
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
			"id": "slow_queries",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please list some of the slowest running queries:",
            "required": false
		}, {
			"id": "query_plan",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please paste your query plan here for the some of the slowest queries:",
			"watermarkText": "Run: EXPLAIN [Your query]; to get the query plan for [Your query]",
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
