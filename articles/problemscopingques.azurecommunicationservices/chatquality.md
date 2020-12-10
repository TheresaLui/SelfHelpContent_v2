<properties
	pageTitle="Chat message quality and performance"
	description="Chat message quality and performance"
	ms.author="manoskow"
	authors="manoskow"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756383, 32756380, 32756372"
	productPesIds="17327"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleID="acs-chatqualityissues"
	ownershipId="AzureCommunicationServices"
	schemaVersion="1"
/>
# Chat quality issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Chat message quality, users and threads, and features",
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
	    "id": "problem_IDs",
	    "order": 4,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Helpful IDs",
	    "watermarkText": "Provide the MS-CV or chat thread ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
	    "required": false
	},
	{
            "id": "problem_description",
            "order": 100,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
