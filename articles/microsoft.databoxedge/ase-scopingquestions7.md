<properties
	pageTitle="Scoping Questions for Azure Stack Edge ports"
	description="Scoping Questions for Azure Stack Edge ports setup"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745980, 32745975, 32745971"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ScopingQuesASEports"
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
	     "id": "Device Connected",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "Is the device is capable of reaching to internet? Check this on the diagnostic tests page",
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
	     "id": "Connected",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "Is the dveice connected to minimum 1Gbe network interface?",
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
	     "id": "Network",
	     "order": 400,
	     "controlType": "dropdown",
	     "displayLabel": "Are we using a network switch to connect or connecting directly from Laptop to the device?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Network_Switch",
                    "text": "Network Switch"
                },
                {
                    "value": "Direct_laptop",
                    "text": "Direct from laptop"
                }
	    ],
            "required": false
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
