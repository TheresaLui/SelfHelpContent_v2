<properties
	pageTitle="Quota increase"
	description="Quota increase for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630561"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="c4db09cc-d1f2-4d55-9344-4806b4bf9d68"
	ownershipId="AzureIot_IotHub"
/>
# Quota increase
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Quota increase",
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
      "id": "event_type",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What limit do you need increasing?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Max paid IoT hubs per subscription",
          "text": "Max paid IoT hubs per subscription"
        },
        {
          "value": "Total device IDs per IoT hub",
          "text": "Total device IDs per IoT hub"
        },
        {
          "value": "Twin size",
          "text": "Twin size"
        },
        {
          "value": "dont_know_answer",
          "text": "Other, don't know, or not applicable"
        }
      ],
      "required": true
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