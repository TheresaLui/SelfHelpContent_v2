<properties
	pageTitle="Availability and Connectivity - Pods,Containers are in a Unhealthy state"
	description="Availability and Connectivity - Pods,Containers are in a Unhealthy state"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747915"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6ec649d4-58f3-4f95-b900-d0bc40c3bafc"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Availability and Connectivity - Pods,Containers are in a Unhealthy state
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Availability and Connectivity - Pods,Containers are in a Unhealthy state",
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
			"id": "error_transient",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Was the error transient or is it still happening?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Transient Error",
					"text": "Transient Error"
				}, {
					"value": "Issue still happening",
					"text": "Issue still happening"
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
			"required": false
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
