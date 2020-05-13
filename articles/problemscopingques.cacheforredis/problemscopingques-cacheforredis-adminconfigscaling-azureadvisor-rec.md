<properties
	pageTitle="Azure Advisor recommendation"
	description="Azure Advisor recommendation"
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
# Azure Advisor recommendation
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
	"title": "Azure Advisor recommendations",
	"fileAttachmentHint": "",
	"formElements": 
    [
        {
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, 
        {
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": 
            [
                {
					"text": "Issue description."
				}, 
                {
					"text": "Issue description"
				}
			]
		}, 
		{
			"id": "Advisor_recommendation",
			"order": 3,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": ""Which Recommendation",
			"watermarkText": "Choose an option",
			"dropdownOptions": 
            [
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
                }
			],
			"required": true
		} 
	]
}

---

