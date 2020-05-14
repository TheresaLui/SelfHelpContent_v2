<properties
	pageTitle="Connection Error"
	description="Connection Error"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690905"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="479ed60f-f55a-4211-9b27-dcc86c42f4eb"
	ownershipId="RedisCache_RedisCache"
/>
# Availability, Connectivity and Timeouts - Connection Error
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Connection Error",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Client_Version",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Version of Client Library",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
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
