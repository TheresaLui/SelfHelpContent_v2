<properties
	pageTitle="Upload and view telemetry SQL MIAA Instance"
	description="Upload and view telemetry SQL MIAA Instance"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747941"
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="285e0665-e181-4f1c-b516-191cb4a3609a"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Upload and view telemetry SQL MIAA Instance
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
			"id": "azure_data_controller_version",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What version of Azure Data Controller are you using? \n Use 'azdata arc dc config show |grep imageTag' to obtain",
			"required": true
		}, {
			"id": "specific_error_message",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which step in the process fails?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "upload",
					"text": "upload"
				}, {
					"value": "export",
					"text": "export"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
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
