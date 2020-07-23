<properties
	pageTitle="Azure Cache for Redis - Diagnostic Logs"
	description="Azure Cache for Redis - Diagnostic Logs"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690910"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="331be567-f024-4cc5-8b8b-ab4fcaf6f265"
	ownershipId="RedisCache_RedisCache"
/>
# Monitoring and Alerting - Critical Alerts
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Diagnostic Logs",
    "fileAttachmentHint": "",
    "formElements": [
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
            "useAsAdditionalDetails": true,
            "watermarkText": "Problem Description",
            "required": true
        },
        {
            "id": "Error_Message",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message",
            "watermarkText": "Error Message",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
