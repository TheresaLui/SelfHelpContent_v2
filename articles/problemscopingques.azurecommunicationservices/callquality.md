<properties
	pageTitle="Poor audio and/or video quality"
	description="Poor audio and/or video quality"
	ms.author="manoskow"
	authors="manoskow"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756378, 32756356, 32756354"
	productPesIds="17327"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="513657ba-4c97-4da7-91c7-be17d8a865b7"
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
			"watermarkText": "Provide the Call ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
			"required": true,
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
