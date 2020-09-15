<properties
	pageTitle="Errors connecting to Kubernetes cluster (kubectl, azdata, etc)"
	description="Errors connecting to Kubernetes cluster (kubectl, azdata, etc)"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743973"
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="6BC37F80-8827-4BD7-85ED-D080E157A6A7"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Errors connecting to Kubernetes cluster (kubectl, azdata, etc)
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
			"displayLabel": "What distribution of Kubernetes are you using?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "AKS",
					"text": "AKS"
				}, {
					"value": "Vanilla Kubernetes",
					"text": "Vanilla Kubernetes"
				}, {
					"value": "OpenShift",
					"text": "OpenShift"
				}, {
					"value": "Azure Stack",
					"text": "Azure Stack"
				}, {
					"value": "EKS",
					"text": "EKS"
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
			"id": "client_tool",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What client tool did you use to create the instance?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "azdata",
					"text": "azdata"
				}, {
					"value": "kubectl",
					"text": "kubectl"
				}, {
					"value": "Azure Data Studio",
					"text": "Azure Data Studio"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "error_message",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "What is the specific error message did you receive?",
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
