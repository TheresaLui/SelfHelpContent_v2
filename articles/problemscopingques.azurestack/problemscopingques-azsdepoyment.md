<properties
    pageTitle="Azure Stack deployment failure"
    description="Azure Stack deployment failure"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629194,32629205"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-9542-4f2d-5238-36a830e63098"
/>
# Azure Stack deployment failure questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack deployment failure questions",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "command_line",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the entered command line used to run the readiness checker?",
            "watermarkText": "",
            "required": false
		},{
            "id": "error_message",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the error output message?",
            "watermarkText": "",
            "required": false
		},{
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": []
		}
	],
  "$schema": "SelfHelpContent"
}
---