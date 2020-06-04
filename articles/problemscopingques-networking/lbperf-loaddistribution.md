<properties
	pageTitle="Load distribution issues"
	description="Load distribution issues"
	authors="ramandhillon84"
	ms.author="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588976"
	productPesIds="16098"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="700961cc-d014-4551-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>

# SLB - Load distribution issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Load distribution issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "config-changes",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Were any configuration changes made to Load Balancer configuration that resulted in the issue?",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "config_lb_nva",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is there a third party virtual appliance (e.g. firewalls, routers) in the data-path?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
            "order": 3,
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
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
