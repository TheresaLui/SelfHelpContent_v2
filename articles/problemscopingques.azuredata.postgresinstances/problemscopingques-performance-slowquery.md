<properties
	pageTitle="Slow Query Performance or Time-outs"
	description="Slow Query Performance or Time-outs"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745092"
	productPesIds="17124"
	cloudEnvironments="Public"
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
			"id": "readwrite",
			"order": 3,
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
			"required": true
		}, {
			"id": "add_workload",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Did you add any workload to your Kubernetes cluster outside of your Azure Arc setup around the time the problem started to occur?",
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
			"id": "client_location",
			"order": 7,
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
			"required": false
		}, {
			"id": "add_workload",
			"order": 8,
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
			"id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
