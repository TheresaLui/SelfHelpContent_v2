<properties
	pageTitle="IoT Hub service issues"
	description="IoT Hub service issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630528"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="dc08c7a8-7b45-4070-9200-20f7ba52bf84"
/>
# IoT Hub service issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "IoT Hub service issues",
  "fileAttachmentHint": "Upload screenshots of errors if available",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "errors",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What error did you see?",
      "watermarkText": "Example: 500001 ServerError",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 10,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        }
      ]
    }
  ]
}
---