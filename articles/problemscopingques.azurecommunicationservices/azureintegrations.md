<properties
	pageTitle="Chat message quality and performance"
	description="Chat message quality and performance"
	ms.author="manoskow"
	authors="manoskow"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756360, 32756363"
	productPesIds="17327"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="acs-chatmessagequality"
	ownershipId="AzureCommunicationServices"
	schemaVersion="1"
/>
# Azure integrations
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "title": "Connecting to Azure Notification Hubs or Event Grid"
  "resourceRequired": true,
  "title": "Connecting to Azure Notification Hubs or Event Grid",
  "fileAttachmentHint": "",
  "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
	},
        {
            "id": "problem end time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem end? If the issue is ongoing leave this blank.",
            "required": false
	},
	{
            "id": "problem_sdk",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the SDK and the version being used for development ",
            "required": false
        },
        {
	    "id": "problem_description",
	    "order": 3,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Helpful IDs",
	    "watermarkText": "Provide the MS-CV or chat thread ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
	    "required": false,
	    "useAsAdditionalDetails": true,
	    "hints": [
	    {
		"text": "MS-CV or chat thread ID"
	    },
	    {
		"text": "Please enter the MS-CV or chat thread ID associated with the Events or Notifications that are failing."
	    }
	    ]
	}
    ]
}
---
