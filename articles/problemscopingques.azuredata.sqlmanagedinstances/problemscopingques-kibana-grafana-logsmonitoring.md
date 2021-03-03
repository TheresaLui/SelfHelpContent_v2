<properties
	pageTitle="Kibana and Grafana logs and Metrics"
	description="Kibana and Grafana logs and Metrics"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32744018"
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="53D87E3D-AD72-44F8-8EB7-BA85B2B8F21C"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Kibana and Grafana Logs and Metrics
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "SQL Server - Azure Arc",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "kubernetes_distribution",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What monitoring component are you using?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Kibana",
					"text": "Kibana"
				}, {
					"value": "Grafana",
					"text": "Grafana"
				}, {
					"value": "Other",
					"text": "Other"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "error_message",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "What is the error message you received?",
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
