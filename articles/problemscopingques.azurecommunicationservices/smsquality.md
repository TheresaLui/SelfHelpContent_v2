<properties
	pageTitle="Poor audio and/or video quality"
	description="Poor audio and/or video quality"
	ms.author="manoskow"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="0f871f84-46d0-f638-d346-5c5a27fe59dd"
	productPesIds="17327"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId=""
	ownershipId="AzureCommunicationServices"
/>
# SMS quality issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "SMS delivery performance and reliability",
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
			"watermarkText": "Provide the MS-CV ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "MS-CV"
				}, {
					"text": "Please enter the MS-CV associated with the message requests that failed or were slow."
				}
			]
		}
	]
}
---
