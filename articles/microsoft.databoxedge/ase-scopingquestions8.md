<properties
	pageTitle="Scoping Questions for Azure Stack Edge ordering"
	description="Scoping Questions for Azure Stack Edge Ordering related"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745967, 32745968, 32745969, 32745990, 32745991, 32745992"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="ScopingQuesASEports"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Edge issues with Ordering
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
	     "id": "Subscription",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "What is your Azure Subscription?",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Enterprise Agreement EA",
                    "text": "Enterprise Agreement - EA"
                },
		{
                    "value": "Cloud Solutions Provider CSP",
                    "text": "Cloud Solutions Provider - CSP"
                },
		{
                    "value": "Micorsoft Azure Sponsorship",
                    "text": "Micorsoft Azure Sponsorship"
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
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/azure-stack-edge-deploy-prep#prerequisites'>Learn more</a> about Azure Stack Edge Pre-requisites"
        }
	],
	"$schema": "SelfHelpContent"
}
---
