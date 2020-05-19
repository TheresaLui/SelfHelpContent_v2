<properties
	pageTitle="CosmosDB Service Unavailability Issue"
	description="CosmosDB Service Unavailability Issue"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636776,32636777,32681008,32681470,32692541"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="cfaed94d-9805-425f-acf5-5e9c8977c657"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Service Unavailability Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Service Unavailability Issue",
    "fileAttachmentHint": "Please attach at least 20 stack traces wtih the exception message in a single flat text file.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "problem_duration",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "How long was the issue observed?",
            "required": false
        },
		{
            "id": "region_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which region is your client running?",
            "required": false
        },
		{
            "id": "sdk_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the client SDK used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": ".NET",
                    "text": ".NET"
                },
                {
                    "value": "Java",
                    "text": "Java"
                },
                {
                    "value": "Node.js",
                    "text": "Node.js"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "REST",
                    "text": "REST"
                }
            ],
            "required": false
        },
		{
            "id": "database_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
		{
            "id": "collection_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": false
        },
		{
            "id": "exception_count",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "How many service unavailable exceptions did you observe?",
            "required": false
        },
		{
            "id": "vm_count",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Number of VMs the exception was seen during this time.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide any additional details about the issue that you were facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Read/Write regions where the issue is experienced"
                },
                {
                    "text": "Activity Id of the request (if available)."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
