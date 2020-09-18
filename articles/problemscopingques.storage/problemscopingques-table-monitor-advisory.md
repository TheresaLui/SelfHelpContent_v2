<properties
	pageTitle="Advisory questions - table"
	description="Advisory questions"
	authors="Sijia"
        ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681647"
	productPesIds="16462"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="01f3daeb-839b-4302-b37e-e8dc32ef447e"
	ownershipId="StorageMediaEdge_StorageTables"
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
                    "value": "log_retention",
                    "text": "Log retention question"
                },
                 {
                    "value": "who_accessed_storage_resource",
                    "text": "Who accessed storage resource"
                },
                 {
                    "value": "table_entities",
                    "text": "Table entities question"
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
            "id": "metrics_help",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which metrics do you need help with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "capacity",
                    "text": "Capacity"
                },
                {
                    "value": "availability",
                    "text": "Availability"
                },
                {
                    "value": "bandwidth",
                    "text": "Bandwidth"
                },
		{
                    "value": "latency",
                    "text": "Latency"
                },
		{
                    "value": "transactions",
                    "text": "Transactions"
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
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
