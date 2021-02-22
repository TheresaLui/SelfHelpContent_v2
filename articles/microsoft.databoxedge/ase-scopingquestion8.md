<properties
	pageTitle="Scoping Questions for Azure Stack Edge Ordering"
	description="Scoping Questions for Azure Stack Edge Ordering"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745990, 32745969, 32745968, 32745967, 32745992"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="SharesScopingQuesASENew"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Edge issues with ordering
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
	     "id": "Subscription Type",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "What is your subscription type",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Enterprise agreement EA",
                    "text": "Enterprise agreement EA"
                },
                {
                    "value": "Cloud Solution Provider CSP",
                    "text": "Cloud Solution Provider CSP"
                },
                {
                    "value": "Microsoft Azure Sponsorship",
                    "text": "Microsoft Azure Sponsorship"
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
            "watermarkText": "Please provide the details regarding the issue, such as an error message that you're receiving.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/azure-stack-edge-gpu-deploy-prep'>Learn more</a> about Azure Stack Edge ordering"
        }
	],
	"$schema": "SelfHelpContent"
}
---
