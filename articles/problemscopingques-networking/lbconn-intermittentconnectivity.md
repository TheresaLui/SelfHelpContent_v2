<properties
	pageTitle="Intermittent connectivity issues"
	description="Intermittent connectivity issues"
	authors="ramandhillon84"
	ms.author="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588975"
	productPesIds="16098"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="700961cc-d014-4554-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>
# SLB - Intermittent connectivity issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Intermittent connectivity issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connectivity_direction",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please specify the connectivity direction",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Inbound to the backend pool",
                    "text": "Inbound to the backend pool"
                },
                {
                    "value": "Outbound from the backend pool",
                    "text": "Outbound from the backend pool"
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
            "displayLabel": "Please specify any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Source / Destination details (e.f. IP Address, URL)"
                },
                {
                    "text": "Did the connectivity work in the past and stopped working now?"
                },
                {
                    "text": "Does the direct access to / from the backend pool instances (without the load balancer IP Address) work?"
                },
                {
                    "text": "Did you recieve any error messages from the Load Balancer that you want to share?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
