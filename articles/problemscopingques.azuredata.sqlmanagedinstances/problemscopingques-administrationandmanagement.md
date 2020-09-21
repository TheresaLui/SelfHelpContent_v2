<properties
	pageTitle="Administration and Management SQL MIAA Instance"
	description="Administration and Management SQL MIAA Instance"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743941"
	productPesIds="17125"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="6FD69F80-A511-4EF1-BA1E-A90A77CC3C72"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Administration and Management SQL MIAA Instance
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
			"id": "area_of_issue",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What specific area is the issue in?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "backup/restore",
					"text": "backup/restore"
				}, {
					"value": "backup",
					"text": "backup"
				}, {
					"value": "file management",
					"text": "file management"
				}, {
					"value": "database consistency",
					"text": "database consistency"
				}, {
					"value": "recovery",
					"text": "recovery"
				}, {
					"value": "startup",
					"text": "startup"
				}, {
					"value": "errors/exceptions",
					"text": "errors/exceptions"
				}, {
					"value": "configuration",
					"text": "configuration"
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
			"displayLabel": "What error message do you receive? ",
			"required": false
		}, {
			"id": "troubleshooting_attempted",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "What troubleshooting steps have you attempted?",
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
