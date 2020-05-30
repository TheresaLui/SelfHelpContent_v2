<properties
	pageTitle="Tier issues"
	description="Tier issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630557"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="4e5c4dbd-00b0-4ce9-b229-d280a7f20847"
	ownershipId="AzureIot_IotHub"
/>
# Tier issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Tier issues",
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
      "displayLabel": "What tier do you want to change to?",
      "watermarkText": "Example: S3",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 10,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true
    }
  ]
}
---