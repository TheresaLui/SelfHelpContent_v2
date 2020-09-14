<properties
	pageTitle="Modify SQL MIAA instance"
	description="Modify SQL MIAA instance"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743990"
	productPesIds="17125"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="1A2002F4-D937-4236-8355-8146F7D1C2FF"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Modify SQL MIAA instance
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
			"id": "azure_data_controller_version",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What version of Azure Data Controller are you using? \n Use 'azdata arc dc config show |grep imageTag' to obtain",
			"required": false
		},{
			"id": "client_tool",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "What client tool did you use to create the instance?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "azdata",
					"text": "azdata"
				}, {
					"value": "kubectl",
					"text": "kubectl"
				},{
					"value": "Azure Data Studio",
					"text": "Azure Data Studio"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "configuration_change",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "What configuration change are you making specifically?",
			"required": false
		}, {
			"id": "error_message",
			"order": 6,
			"controlType": "multilinetextbox",
			"displayLabel": "What is the specific error message did you receive?",
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
