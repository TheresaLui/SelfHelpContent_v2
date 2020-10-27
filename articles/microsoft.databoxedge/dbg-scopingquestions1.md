<properties
	pageTitle="Scoping Questions for Databox Gateway"
	description="Scoping Questions for DBG"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745315, 32745311, 32745314, 32745316, 32745309, 32745317, 32745313, 32745312, 32745320, 32745305, 32745321"
	productPesIds="17315"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ScopingQuesDBG"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box gateway generic
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure DBG issues",
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
	     "id": "Heartbeat",
	     "order": 100,
	     "controlType": "dropdown",
	     "displayLabel": "Is the device pingable?",
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
	     "id": "Network",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": " Do we have the device connected to minimum 1Gbe network interface?",
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
            "watermarkText": "Please provide the details regarding the issue, such as the error message that you are receiving.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/data-box-gateway-deploy-connect-setup-activate'>Learn more</a> about Azure DataBox Deployment"
        }
	],
	"$schema": "SelfHelpContent"
}
---
