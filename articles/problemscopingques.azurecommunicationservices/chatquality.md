<properties
	pageTitle="Chat message quality and performance"
	description="Chat message quality and performance"
	ms.author="manoskow"
	authors="manoskow"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756357, 32788595, 32789474"
	productPesIds="17327"
	cloudEnvironments="public"
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
            "id": "Platform",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Client platform you are experiencing issues with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "iOS",
                    "text": "iOS"
                },
                {
                    "value": "Android",
                    "text": "Android"
                },
		{
		    "value":"Web",
		    "text":"Web"
		},
		{
		    "value":"Multiple",
		    "text":"Multiple"
		},
    	        {
    	    	    "text": "Don't know or not applicable"
		    "value": "dont_know_answer"
    	        }
	    ],
            "required": true
	},
        {
	    "id": "problem_IDs",
	    "order": 4,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Helpful information includes the MS-CV, Thread ID, SDK version, and Teams tenant ID for Teams Interop issues. For more details see https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info.",
	    "watermarkText": "Provide the MS-CV, Thread ID, SDK Version, and Teams tenant ID (in case of Teams Interop issues).",
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
