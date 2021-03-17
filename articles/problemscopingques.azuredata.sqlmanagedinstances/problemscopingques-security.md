<properties
	pageTitle="Security SQL MIAA Instance"
	description="Security SQL MIAA Instance"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743948"
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="7F1AEFDE-23E9-4E5E-B193-D9D631B98412"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Security SQL MIAA Instance
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
			"id": "area_of_security_issue",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What security area is the issue in?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Authentication",
					"text": "Authentication"
				}, {
					"value": "Authorization",
					"text": "Authorization"
				}, {
					"value": "Encryption",
					"text": "Encryption"
				}, {
					"value": "Auditing",
					"text": "Auditing"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "describe",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Describe the security issue",
			"required": false
		}, {
			"id": "error_message",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "What error message are you getting, if any?",
			"required": false
		}, {
			"id": "troubleshooting_attempted",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "What troubleshooting steps have you attempted?",
			"required": false
		}, {
			"id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
