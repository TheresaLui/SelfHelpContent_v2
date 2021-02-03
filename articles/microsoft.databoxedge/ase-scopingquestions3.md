<properties
	pageTitle="Scoping Questions for Azure Stack Edge Shares and Data Tiering"
	description="Scoping Questions for Azure Stack Edge Shares and Data Tiering"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745994, 32745977, 32745984, 32745985, 32745986, 32745987, 32745989"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="SharesScopingQuesASE"
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
	     "displayLabel": "Is the device capable of reaching internet - can check in Diagnostic test page?",
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
	     "id": "Network Configuration",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "Check the network configuration from WebUI - is it DHCP or Static?",
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
                    "text": "Other, don't know or not applicable"
                }
	    ],
            "required": true
        },
	{
	     "id": "Support Package",
	     "order": 500,
	     "controlType": "dropdown",
	     "displayLabel": "Are you able to download and send support package?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "Do_not_know",
                    "text": "Do not know"
                },
                {
                    "value": "already_done",
                    "text": "Have already done"
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
