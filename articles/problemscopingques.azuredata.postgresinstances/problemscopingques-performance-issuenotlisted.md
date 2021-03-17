<properties
	pageTitle="Slow Performance - My issue is not listed"
	description="Slow Performance - My issue is not listed"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745075"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="53c2ddca-f1c5-4ff7-8535-d84e51830dd5"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Slow Performance - My issue is not listed
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Slow Performance - My issue is not listed",
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
			"id": "reproducible",
			"order": 3,
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
			"id": "workload",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Has your workload increased during this time?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "True",
					"text": "True"
				}, {
					"value": "False",
					"text": "False"
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
			"id": "what_changed",
			"order": 6,
			"visibility": "servergroup_config == Yes",
			"controlType": "multilinetextbox",
			"displayLabel": "What configuration did you change?",
			"watermarkText": "Provide details about configuration change.",
            "required": false
		}, {
			"id": "type_kubernetes",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Types of Kubernetes clusters or managed Kubernetes services you are using",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Azure Kubernetes Service (AKS)",
					"text": "Azure Kubernetes Service (AKS)"
				}, {
					"value": "Azure Kubernetes Engine (AKE) on Azure Stack",
					"text": "Azure Kubernetes Engine (AKE) on Azure Stack"
				}, {
					"value": "OpenShift Container Platform (OCP) 4.2+",
					"text": "OpenShift Container Platform (OCP) 4.2+"
				}, {
					"value": "Azure RedHat OpenShift (ARO)",
					"text": "Azure RedHat OpenShift (ARO)"
				}, {
					"value": "Open source, upstream Kubernetes",
					"text": "Open source, upstream Kubernetes version 1.14+ using kubeadm"
				}, {
					"value": "AWS Elastic Kubernetes Service (EKS)",
					"text": "AWS Elastic Kubernetes Service (EKS)"
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
