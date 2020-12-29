<properties
	pageTitle="Scoping Questions for Azure Stack Edge Compute"
	description="Scoping Questions for Azure Stack Edge Compute"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745973, 32745976, 32745981"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ComputeScopingQuesASE"
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
	     "id": "Proxy Server",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "Are you using any kind of Proxy server to communicate?",
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
	     "id": "IOT Hub",
	     "order": 400,
	     "controlType": "dropdown",
	     "displayLabel": " Is the issue happening only while creating IoT modules with existing IoT hub ? what happens if we create a new IoT hub?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Not_tested",
                    "text": "Not Tested"
                },
		{
                    "value": "Issue_with_both",
                    "text": "Issue with new IOT Hub also"
                },
                {
                    "value": "Resolved",
                    "text": "Resolved with new IOT Hub"
                }
	    ],
            "required": false
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
