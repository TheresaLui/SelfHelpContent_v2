<properties
	pageTitle="Scoping Questions for Databox Gateway"
	description="Scoping Questions for DBG"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745310, 32745307"
	productPesIds="17315"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ScopingQuesDBGPNetwork"
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
	     "id": "Connection",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "Are you using a network switch to connect or connecting directly from Laptop to the device?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "NetworkSwitch",
                    "text": "NetworkSwitch"
                },
		{
                    "value": "Direct from system",
                    "text": "Direct from system"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                }
	    ],
            "required": true
        },
	{
	     "id": "Configuration",
	     "order": 500,
	     "controlType": "dropdown",
	     "displayLabel": "Check for network configuration from Web UI? DHCP or static.",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "DHCP",
                    "text": "DHCP"
                },
		{
                    "value": "Static",
                    "text": "Static"
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
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/data-box-gateway-deploy-connect-setup-activate'>Learn more</a> about Azure DataBox Deployment"
        }
	],
	"$schema": "SelfHelpContent"
}
---
