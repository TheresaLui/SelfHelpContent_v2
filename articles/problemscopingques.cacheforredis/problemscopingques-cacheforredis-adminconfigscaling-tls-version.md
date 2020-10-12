<properties
	pageTitle="Azure Cache for Redis - TLS Version"
	description="Azure Cache for Redis - TLS Version"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690920"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="4b25cad5-810f-4978-953c-4eaaa7ee8af6"
	ownershipId="RedisCache_RedisCache"
/>
# Administration, Configuration and Scaling - TLS Version
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "TLS Version",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Redis_Client",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Name of Redis Client Library used (StackExchange.Redis, Jedis, etc.)",
            "watermarkText": "Redis Client",
            "required": true
        },
        {
            "id": "Error_Message",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message",
            "watermarkText": "Error Message",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem Description",
            "watermarkText": "Problem Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---