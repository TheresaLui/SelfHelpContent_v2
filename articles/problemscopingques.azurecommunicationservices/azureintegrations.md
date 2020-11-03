<properties
	pageTitle="Chat message quality and performance"
	description="Chat message quality and performance"
	ms.author="manoskow"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="583bde8b-f55a-ad1a-c200-f8e8e8f4cc43","dde907b2-7a99-e332-b8c1-bfcbaa19dd2e"
	productPesIds="17327"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
	ownershipId="AzureCommunicationServices"
/>
# Azure integrations
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Connecting to Azure Notification Hubs or Event Grid",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },  {
			"id": "problem_description",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Helpful IDs",
			"watermarkText": "Provide the MS-CV or chat thread ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "MS-CV or chat thread ID"
				}, {
					"text": "Please enter the MS-CV or chat thread ID associated with the Events or Notifications that are failing."
				}
			]
		}
	]
}
---
