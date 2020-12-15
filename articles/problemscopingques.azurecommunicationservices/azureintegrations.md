<properties
	pageTitle="Azure Integrations with Azure Communication Services"
	description="Azure Integrations with Azure Communication Services"
	ms.author="manoskow"
	authors="manoskow"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756360, 32756363"
	productPesIds="17327"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5bb9aec7-eead-4c8a-8dd5-c582d88a71a5"
	ownershipId="AzureCommunicationServices"
	schemaVersion="1"
/>
# Azure integrations
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
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
	    "id": "problem_IDs",
	    "order": 4,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Helpful IDs",
	    "watermarkText": "Provide the MS-CV, Call ID, or chat thread ID to help us troubleshoot the issue. Follow <a href='https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info'>instructions here</a> for how to collect this information",
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
