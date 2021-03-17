<properties
	pageTitle="Security - My issue is not listed"
	description="Security - My issue is not listed"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745074"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="74cf5c53-35fb-475c-8461-6c1d20ae577c"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Security - My issue is not listed
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Security - My issue is not listed",
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
			"id": "tool",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What tool did you use?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "CLI azdata",
					"text": "CLI azdata"
				}, {
					"value": "CLI kubectl",
					"text": "CLI kubectl"
				}, {
					"value": "Azure Data Studio",
					"text": "Azure Data Studio"
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
			"id": "type_kubernetes",
			"order": 4,
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
