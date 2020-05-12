<properties
	pageTitle="No connectivity to the backend pool"
	description="No connectivity to the backend pool"
	authors="ramandhillon84"
	ms.author="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588977"
	productPesIds="16098"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="700961cc-d014-4555-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>
# SLB - No connectivity to the backend pool
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "No connectivity to the backend pool",
    "fileAttachmentHint": "",
    "formElements": [
           {
            "id": "is_backend_issue",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Can you access the backend pool instance directly without the load balancer?",
             "infoBalloonText": "If no, this issue should not be considered as a load balancer issue. You need to fix the connectivity issue with the backed pool instances first.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes. "
                },
                {
                    "value": "No",
                    "text": "No."
                },
                {
                    "value": "dont_know_answer",
                    "text": "I didn't try"
                }
            ],
            "required": true
        },
        {
            "id": "inbound-connectivity",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please specify the source location",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Within virtual network",
                    "text": "Within virtual network"
                },
                {
                    "value": "A peered virtual network in the same region",
                    "text": "A peered virtual network in the same region"
                },
                {
                    "value": "A peered virtual network in a different region",
                    "text": "A peered virtual network in a different region"
                },
                {
                    "value": "External Internet endpoint",
                    "text": "External Internet endpoint"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "connectivity-break-type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Please specify the type of connectivity loss",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Intermittent connectivity loss",
                    "text": "Intermittent connectivity loss"
                },
                {
                    "value": "Persistent problem",
                    "text": "Persistent problem"
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
            "order": 4,
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
                    "text": "Source details (e.f. IP Address)"
                },
                {
                    "text": "Did the connectivity work in the past and stopped working now?"
                },
                {
                    "text": "Did you receive any error messages from the Load Balancer that you want to share?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---