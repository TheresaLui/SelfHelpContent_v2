<properties
	pageTitle="Scoping Questions for Azure Stack Edge Set up and configuration"
	description="Scoping Questions for Azure Stack Edge Set up and configuration"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745979,32745988"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="newScopingQuesASE"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Edge issues with setup and configuration
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Stack Edge issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the problem first observed?",
            "required": true
        },
        {
            "id": "were_changes_done",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Were there any changes done, post which you started seeing this issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "previous_solution",
            "visibility": "were_changes_done == Yes",
            "order": 110,
            "controlType": "multilinetextbox",
            "displayLabel": "List the changes which were made",
            "watermarkText": "Describe in detail the changes which were made",
            "required": false
        },
	{
	     "id": "Device Connected",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "Is the Device capable of reaching Internet? Can check on Doagnostics Test page",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "On",
                    "text": "On"
                },
                {
                    "value": "Off",
                    "text": "Off"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details regarding the issue, such as Error that you are getting.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/azure-stack-edge-deploy-connect-setup-activate'>Learn more</a> about Azure Stack Edge Setup"
        }
	],
	"$schema": "SelfHelpContent"
}
---
