<properties
	pageTitle="Advisory questions - Blob, ADLS Gen2 - excluding metrics ST"
	description="Advisory questions"
	authors="Sijia"
        ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681424,32681422,32681425,32681657"
	productPesIds="16459,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="c449c5cc-78a3-4ef0-88a0-3c4622437a24"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Monitoring - Advisory questions
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Monitoring advisory questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Need advisory on Monitoring related questions?",
        "description": "Our Monitor Advisory troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure the information provided is accurate and in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
	},
    "formElements": [
        {
            "id": "monitor_advisory",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Monitor advisory question",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "cost_question",
                    "text": "Cost related question"
                },
                {
                    "value": "container_capacity",
                    "text": "Container capacity question"
                },
                {
                    "value": "log_retention",
                    "text": "Log retention question"
                },
                {
                    "value": "audit_action",
                    "text": "Action audit question"
                },
		 {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
