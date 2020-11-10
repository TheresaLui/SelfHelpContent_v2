<properties
	pageTitle="Chat message quality and performance"
	description="Chat message quality and performance"
	ms.author="manoskow"
	authors="manoskow"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756383, 32756380, 32756372"
	productPesIds="17327"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
	ownershipId="AzureCommunicationServices"
/>
# Chat quality issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Chat message delivery quality, performance, managing threads and users, read receipts and typing indicators",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },  {
			"id": "problem_description",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Helpful IDs",
			"watermarkText": "Provide the MS-CV or chat thread ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "MS-CV or chat thread ID"
				}, {
					"text": "Please enter the MS-CV or chat thread ID associated with the chat messages that are failing."
				}
			]
		}
	]
}
---
