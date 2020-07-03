<properties
	pageTitle="Errors and exceptions scoping questions"
	description="Scoping questions to capture more details about errors and exceptions"
	ms.author="lyhughes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32571145"
	productPesIds="16244"
	cloudEnvironments="public, mooncake"
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
	"fileAttachmentHint": "",
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
			"order": 2,
			"controlType": "textblock",
			"displayLabel": "What specific error code are you getting (400, 404, 500)",
			"watermarkText": "Provide any error message that you're seeing",
			"required": false,
			"useAsAdditionalDetails": false
		},
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
	]
}
---