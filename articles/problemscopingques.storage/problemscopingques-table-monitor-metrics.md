<properties
	pageTitle="Advisory questions - table"
	description="Advisory questions"
	authors="Lea"
        ms.author="leakkari"
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
            "id": "table_names",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Table Names",
            "watermarkText": "Select from your tables",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/tableServices/default/tables?api-version=2019-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No tables available"
                    }
            }
        },
        {
            "id": "monitor_advisory",
            "order": 2,
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
            "order": 3,
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
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
           "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "watermarkText": "Enter one question at a time. Example: What is Azure Monitor?",
            "displayLabel": "Enter your question",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
