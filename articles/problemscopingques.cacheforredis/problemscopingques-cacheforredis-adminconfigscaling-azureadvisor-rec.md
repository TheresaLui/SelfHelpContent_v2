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
    "title": "Failure to connect to the VM using Azure Bastion",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "bastionbrowser",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What browser are you using?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "bastionbrowserversion",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What version is your browser?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "bastionbrowseros",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What OS is your browser running in?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "Advisor_recommendation",
            "order": 6,
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
            "order": 14,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 15,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ]
}
---
