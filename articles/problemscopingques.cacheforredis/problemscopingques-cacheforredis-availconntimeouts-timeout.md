<properties
	pageTitle="Azure Cache for Redis - Timeout"
	description="Azure Cache for Redis - Timeout"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690919"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="31a3c862-9f31-4cad-b4cd-dbfc43fcbee4"
	ownershipId="RedisCache_RedisCache"
/>
# Availability, Connectivity and Timeouts - Timeout
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Timeout",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem End?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description of Problem",
            "watermarkText": "Description of Problem",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "Stack_Trace",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Error and Stack Trace of errors on the client",
            "watermarkText": "Stack Trace of errors",
            "required": true
        },
        {
            "id": "Client_LIbrary",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Name of Redis Client Library used (StackExchange.Redis, Jedis, etc.)",
            "watermarkText": "Redis Client Library",
            "required": false
        },
        {
            "id": "Client_Version",
            "order": 6,
            "controlType": "radioButtonGroup",
            "displayLabel": "Version of Client Library",
            "watermarkText": "Choose an option",
            "radioButtonOptions": [
                {
                    "value": "NuGet Package version of StackExchange.Redis",
                    "text": "NuGet Package version of StackExchange.Redis"
                },
                {
                    "value": "Microsoft.Web.RedisSessionStateProvider",
                    "text": "Microsoft.Web.RedisSessionStateProvider"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "Config_Details",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Redis Client Library configuration details",
            "watermarkText": "Configuration Details",
            "required": false
        }
    ]
}
---
