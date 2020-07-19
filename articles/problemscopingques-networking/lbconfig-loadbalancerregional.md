<properties
	pageTitle="Configure a Zone Redundant Load Balancer"
	description="Configure a Zone Redundant Load Balancer"
	authors="ramandhillon84"
	ms.author="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608575"
	productPesIds="16098"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="700961cc-d014-4548-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>
# SLB - Configure a Zone Redundant Load Balancer
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Configure a Zone Redundant Load Balancer",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "config_regional_lb",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the Load Balancer resource type that you need help with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Internal Load Balancer",
                    "text": "Internal Load Balancer"
                },
                {
                    "value": "Public Load Balancer",
                    "text": "Public Load Balancer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please specify any additional details or questions",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Do you need help with any specific configuration problem?"
                },
                {
                    "text": "Did you recieve any error messages while configuring a Load Balancer? (If yes, please share the error message as well)"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
