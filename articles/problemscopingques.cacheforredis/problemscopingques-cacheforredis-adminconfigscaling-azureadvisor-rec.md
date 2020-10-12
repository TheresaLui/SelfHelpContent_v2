<properties
	pageTitle="Azure Cache for Redis - Azure Advisor recommendation"
	description="Azure Cache for Redis - Azure Advisor recommendation"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690904"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="8f0d05aa-d988-4078-9fa1-6efe8ff4a83f"
	ownershipId="RedisCache_RedisCache"
/>
# Administration, Configuration and Scaling - Azure Advisor recommendation
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Advisor recommendation",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Advisor_recommendation",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select Advisor Recommendation",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "High Availability",
                    "text": "High Availability"
                },
                {
                    "value": "Performance",
                    "text": "Performance"
                },
                {
                    "value": "Operational Excellence",
                    "text": "Operational Excellence"
                },
                {
                    "value": "Cost",
                    "text": "Cost"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                   {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
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
        },
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ]
}
---
