<properties
	pageTitle="Errors and exceptions scoping questions"
	description="Scoping questions to capture more details about errors and exceptions"
	ms.author="lyhughes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32571145"
	productPesIds="16244"
	cloudEnvironments="public, mooncake, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="969d90c5-c125-470a-9822-4759ffea4939"
	ownershipId="AzureIot_IotTSI"
/>
# Errors and exceptions scoping questions
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Errors and Exceptions",
	"fileAttachmentHint": "If applicable, upload a screenshot of your error",
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "What specific error code, if any, are you getting (400, 404, 500)"
				}
			]
		}
	]
}
---