<properties
	pageTitle="Poor audio and/or video quality"
	description="Poor audio and/or video quality"
	ms.author="manoskow"
	authors="manoskow"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32756378, 32756356, 32756354"
	productPesIds="17327"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="513657ba-4c97-4da7-91c7-be17d8a865b7"
	ownershipId="AzureCommunicationServices"
	schemaVersion="1"
/>
# Call quality issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Audio/video quality, no ringing signal, and call drops ",
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
            "order": 5,
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
	    ],
            "required": true
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
	    "displayLabel": "Helpful information includes Call ID, SDK version, Teams tenant ID for Teams Interop issues. For more details see https://docs.microsoft.com/azure/communication-services/concepts/troubleshooting-info.",
	    "watermarkText": "Provide the Call ID, SDK Version, and Teams tenant ID (in case of Teams Interop issues).",
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
