<properties
	pageTitle="View Server Group resources on Azure Portal"
	description="View Server Group resources on Azure Portal"
	ms.author="amigan,pookam,babarmav"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32747919"
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="0aabe254-23fe-48be-b238-3e906b765846"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
/>
# View Server Group resources on Azure Portal
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "View Server Group resources on Azure Portal",
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
			"id": "upload_azure",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Have you uploaded metrics/logs or usage data to Azure?",
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
			"id": "servergroup",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Are you unable to see your Server Group in the Portal?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes, unable to see",
					"text": "Yes, unable to see"
				}, {
					"value": "Server Group visible, but has stale information",
					"text": "Server Group visible, but has stale information"
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
