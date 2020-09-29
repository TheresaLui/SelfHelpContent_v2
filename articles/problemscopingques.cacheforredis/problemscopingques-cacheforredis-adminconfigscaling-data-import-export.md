<properties
	pageTitle="Azure Cache for Redis - Data Import or Export"
	description="Azure Cache for Redis - Data Import or Export"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
    useAsAdditionalDetails="true" 
	supportTopicIds="32690908"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="d45359e1-ea36-4b75-8bc0-b71aaf983263"
	ownershipId="RedisCache_RedisCache"
/>

# Administration, Configuration and Scaling - Data Import or Export
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Data Import or Export",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Storage_Account",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Storage Account",
            "watermarkText": "Storage Account",
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