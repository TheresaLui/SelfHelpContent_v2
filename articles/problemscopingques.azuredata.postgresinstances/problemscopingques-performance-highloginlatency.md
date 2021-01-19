<properties
	pageTitle="High Login Latency"
	description="High Login Latency"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745062"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="59d0b65d-6d81-4ec7-a8c3-c1de8e195c9b"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# High Login Latency
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "High Login Latency",
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
			"displayLabel": "Where is your client located relative to your database server?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Hosted in the same Kubernetes cluster",
					"text": "Hosted in the same Kubernetes cluster"
				}, {
					"value": "In the same datacenter",
					"text": "In the same datacenter"
				}, {
					"value": "Near the datacenter",
					"text": "Near the datacenter"
				}, {
					"value": "Far from the datacenter",
					"text": "Far from the datacenter"
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
			"required": true
		}, {
			"id": "point_of_comparison",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What is your point of comparison?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Slower than Database running locally",
					"text": "Slower than Database running locally"
				}, {
					"value": "Slower than server in another Azure Arc Environment",
					"text": "Slower than server in another Azure Arc Environment"
				}, {
					"value": "Slower than it typically is in the same Azure Arc environment",
					"text": "Slower than it typically is in the same Azure Arc environment"
				}, {
					"value": "Other",
					"text": "Other"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": false
		}, {
			"id": "concurrent_connections",
			"order": 6,
			"controlType": "textbox",
			"displayLabel": "How many concurrent connections are established on your database server approximatively?",
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
