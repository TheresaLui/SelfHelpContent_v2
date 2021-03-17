<properties
	pageTitle="Questions on Supported K8s and cluster pre-requisites"
	description="Questions on Supported K8s and cluster pre-requisites"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747917"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="a267f247-422d-4a22-960d-7dea9237974e"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# Questions on Supported K8s and cluster pre-requisites
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "Questions on Supported K8s and cluster pre-requisites",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "type_kubernetes",
			"order": 2,
			"controlType": "multiselectdropdown",
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
