<properties
	pageTitle="Poor audio and/or video quality"
	description="Poor audio and/or video quality"
	ms.author="manoskow"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="86f83266-c0bd-6b3c-4d5b-b3c8c9fdb6bc","b7a34672-67b2-aac0-5b2e-972c813b6892","ef219c49-a994-47fa-fbd3-77f9b7a8d443"
	productPesIds="17327"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
	ownershipId="AzureCommunicationServices"
/>
# Call quality issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Poor audio/video quality, call drops, and no ringing signal",
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
			"watermarkText": "Provide the Call ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Call ID"
				}, {
					"text": "Please enter the Call ID associated with the calls that have poor quality."
				}
			]
		}
	]
}
---
