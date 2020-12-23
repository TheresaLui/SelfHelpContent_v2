<properties
	pageTitle="IoT Hub manual failover issues"
	description="IoT Hub manual failover issues for IoT Hub scoping questions"
	authors="camanle"
	ms.author="camanle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630558"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-manual-failover"
	ownershipId="AzureIot_IotHub"
/>
# IoT Hub Manual Failover issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "IoT Hub Manual Failover issues",
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
      "id": "failover",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "How are you initiating manual failover?",
      "required": false
    }
  ]
}
---