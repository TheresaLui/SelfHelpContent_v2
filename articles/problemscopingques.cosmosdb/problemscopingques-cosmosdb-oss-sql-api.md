<properties
	pageTitle="CosmosDB OSS SQL API scoping questions"
	description="CosmosDB OSS SQL API scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636770,32636774,32783702,32741534"
    productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="c506ee0d-d6c5-41fe-9690-36469cf91f2e"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB OSS SQL API
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB OSS SQL API",
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
            "id": "database_name",
            "order": 2,
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
            "order": 3,
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
            "id": "oss_api",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which API are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Core (SQL)",
                    "text": "Core (SQL)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
		{
            "id": "sdk_type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Which SDK are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": ".NET",
                    "text": ".NET"
                },
                {
                    "value": ".NET Core",
                    "text": ".NET Core"
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
                    "value": "Spring Boot",
                    "text": "Spring Boot"
                },
                {
                    "value": "REST",
                    "text": "REST"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1.x.x, 2.x.x, 3.x.x, 4.x.x, etc.)",
            "required": false
        },
        {
            "id": "issue_frequency",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "How frequent is the issue?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing",
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
