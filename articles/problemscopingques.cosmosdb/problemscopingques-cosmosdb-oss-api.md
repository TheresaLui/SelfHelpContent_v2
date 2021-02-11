<properties
	pageTitle="CosmosDB OSS API scoping questions"
	description="CosmosDB OSS API scoping questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636750,32636769,32636782,32636787,32741537,32783703,32636817,32636830,32636770,32636774,32688843,32783702,32741534,32746031,32675631,32783707,32675633,32783708,32675634,32675635,32675638,32636831,32747699,32636789,32783701,32783714,32636819,32738475"
    productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="96cc9e16-5378-4d6e-a8c4-1b23c66994bf"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB OSS API
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB OSS API",
    "fileAttachmentHint": "",
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
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.DocumentDB/databaseAccounts/{resourcename}/sqlDatabases?api-version=2020-04-01",
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
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.DocumentDB/databaseAccounts/{resourcename}/sqlDatabases/{replaceWithParentValue}/containers?api-version=2020-04-01",
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
                    "value": "Azure Table",
                    "text": "Azure Table"
                },
                {
                    "value": "Cassandra API",
                    "text": "Cassandra API"
                },
                {
                    "value": "Core (SQL)",
                    "text": "Core (SQL)"
                },
                {
                    "value": "Gremlin (Graph)",
                    "text": "Gremlin (Graph)"
                },
                {
                    "value": "MongoDB",
                    "text": "MongoDB"
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
