<properties
	pageTitle="Outbound connectivity failures"
	description="Outbound connectivity failures"
	authors="ramandhillon84"
	ms.author="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608577"
	productPesIds="16098"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="700961cc-d014-4550-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>
# SLB - Outbound connectivity failures
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Outbound connectivity failures",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "outbound-connectivity",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please specify the destination location",
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
            "order": 2,
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
            "id": "config_lb_nva",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is there a third party virtual appliance (e.g. firewalls, routers) in the data-path that are being used for outbound connectivity?",
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
                    "text": "Destination details (e.f. IP Address, URL)"
                },
                {
                    "text": "Did the connectivity work in the past and stopped working now?"
                },
                {
                    "text": "Can you access the destination from the backend pool instances directly?"
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
