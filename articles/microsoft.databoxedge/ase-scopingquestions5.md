<properties
	pageTitle="Scoping Questions for Azure Stack Edge RunTime"
	description="Scoping Questions for Azure Stack Edge RunTime"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745972"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="RuntimeScopingQuesASE"
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
	     "id": "Verify Network",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "Verify compute network settings, make sure the IPs provided are continuous and not duplicate?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                },
                {
                    "value": "already_done",
                    "text": "Have already done"
                }
	    ],
            "required": true
        },
	{
	     "id": "Runtime Status",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "What is the runtime status of the Modules- Running or BackOff?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Running",
                    "text": "Running"
                },
		{
                    "value": "Backoff",
                    "text": "Backoff"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                }
	    ],
            "required": true
        },
	{
	     "id": "Custom Docker",
	     "order": 400,
	     "controlType": "dropdown",
	     "displayLabel": " Are you using custom docker image for modules?",
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
                    "text": "Do not know"
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
