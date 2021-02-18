<properties
	pageTitle="CosmosDB OSS SQL Connectivity API scoping questions"
	description="CosmosDB OSS SQL Connectivity API scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32681470"
    productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="8f63c742-db58-49c5-af2c-6e824eb4b6c8"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB OSS SQL Connectivity API
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB Service Unavailability Issue",
    "fileAttachmentHint": "Please attach at least 20 stack traces with the exception message in a single flat text file.",
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
            "controlType": "dropdown",
            "displayLabel": "Database name",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.DocumentDB/databaseAccounts/{resourcename}/sqlDatabases?api-version=2021-01-15",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Select Database Name"
                }
            },
            "required": true
        },
		{
            "id": "collection_name",
            "order": 6,
            "visibility": "database_name != null",
            "controlType": "dropdown",
            "displayLabel": "Collection name",
            "dynamicDropdownOptions": {
                "dependsOn": "database_name",
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.DocumentDB/databaseAccounts/{resourcename}/sqlDatabases/{replaceWithParentValue}/containers?api-version=2021-01-15",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Select Collection Name"
                },
                "valuePropertyRegex":  "[^/]+$"
            },
            "required": true
        },
		{
            "id": "exception_message",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What is the exception message?",
            "required": false
        },
		{
            "id": "exception_count",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "How many exceptions did you observe?",
            "required": false
        },
		{
            "id": "vm_count",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Number of VMs that the exception was seen during this time.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
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
