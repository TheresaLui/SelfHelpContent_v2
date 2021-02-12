<properties
	pageTitle="Azure Cache for Redis - High Latency"
	description="Azure Cache for Redis - High Latency"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690912"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="b31dcf3e-693f-4df4-b3c7-61b239e132b134"
	ownershipId="RedisCache_RedisCache"
/>
# Latency and Throughput - High Latency
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "High Latency",
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description of Problem",
            "watermarkText": "Description of Problem",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "Client_LIbrary",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Name of Redis Client Library used (StackExchange.Redis, Jedis, etc.)",
            "watermarkText": "Redis Client Library",
            "required": true
        },
        {
            "id": "Client_Version",
            "order": 4,
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
            "id": "Stack_Trace",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Error and Stack Trace of errors on the client",
            "watermarkText": "Stack Trace of errors",
            "required": false
        }
    ]
}
---
