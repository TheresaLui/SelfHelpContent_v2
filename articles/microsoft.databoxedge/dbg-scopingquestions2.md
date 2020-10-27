<properties
	pageTitle="Scoping Questions for Databox Gateway"
	description="Scoping Questions for DBG"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745318, 32745319"
	productPesIds="17315"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ScopingQuesDBGProvisioning"
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
	     "id": "Provisioning",
	     "order": 100,
	     "controlType": "dropdown",
	     "displayLabel": "Did you meet the minimum requirements of 4 vcpu and 2 TB virtual disk?",
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
	     "displayLabel": " Do you have the device connected to minimum 1Gbe network interface?",
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
