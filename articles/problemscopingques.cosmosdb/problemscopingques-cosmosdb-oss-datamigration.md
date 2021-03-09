<properties
	pageTitle="CosmosDB OSS Data Migration scoping questions"
	description="CosmosDB OSS Data Migration questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32788295,32788297,32788299,32788296,32788298"
    productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="a7950f46-dd38-4407-b1aa-eaa8820ea264"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Data Migration
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
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
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
        {
            "id": "collection_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": false
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
