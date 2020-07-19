<properties
	pageTitle="CosmosDB SDK Latency Issues"
	description="CosmosDB SDK Latency Issues"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688841"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="e00c06b2-121f-4f8b-84a1-0a8c0eae18e5"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB SDK Latency Issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB SDK Latency Issues",
    "fileAttachmentHint": "Please (zip) attach a .csv with extra request diagnostics or query metrics if available, as well additional debugging info like a repro.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "previous_steps",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What steps have you taken to resolve the issue?",
			"infoBallonText": "Provide steps and include URLs to documents, git hub, stack overflow, forms, etc. that you have already searched to help us improve",
			"required": false
        },
		{
            "id": "cpu_information",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "CPU Information",
            "required": false
        },
		{
            "id": "environment_information",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Environment Information",
			"infoBalloonText": "Environment info (Azfunctions/App Service/VM, Other, Spark, Spring, Other Cloud)",
            "required": false
        },
		{
            "id": "region_information",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Region Information",
			"infoBalloonText": "Read/Write regions where the issue is experienced",
            "required": false
        },
		{
            "id": "request_pct",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Percentage of requests observing latency",
            "required": false
        },
		{
            "id": "sdk_type",
            "order": 7,
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
                    "value": "Java Script or Node.js",
                    "text": "Java Script or Node.js"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "Spring",
                    "text": "Spring"
                },
                {
                    "value": "Spark",
                    "text": "Spark"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1.x.x, 2.x.x, 3.x.x)",
            "required": false
        },
		{
            "id": "query_string",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Request Diagnostics or Query Metrics string",
			"infoBalloonText": "<a href='https://docs.microsoft.com/azure/cosmos-db/troubleshoot-dot-net-sdk'>Cosmos DB article</a> - Diagnostics how to",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---