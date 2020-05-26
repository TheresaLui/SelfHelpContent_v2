<properties
	pageTitle="IoT Central service issues"
	description="IoT Central service issues for IoT Central scoping questions"
	authors="jlian"
	ms.author="jajens"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32592896,32592872,32592871,32592894,32592900"
	productPesIds="16284"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="0f6076df-449f-42da-9686-de2ada7362ba"
	ownershipId="AzureIot_IotCentral"
/>
# IoT Central service issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "IoT Central service issues",
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
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Description of the issue and repro steps"
        },
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        }
      ]
    },
    {
      "id": "errors",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "What error did you see?",
      "watermarkText": "Example: Error Code 500.000.999.999 / bk83coy1.1",
      "required": false
    }
  ]
}
---