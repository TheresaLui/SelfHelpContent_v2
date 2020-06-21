<properties
	pageTitle="Configure an IPv6 Load Balancer"
	description="Configure an IPv6 Load Balancer"
	authors="ramandhillon84"
	ms.author="rdhillon"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32588971"
	productPesIds="16098"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="700961cc-d014-4547-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>
# SLB - Configure an IPv6 Load Balancer
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Configure an IPv6 Load Balancer",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "config_ipv6_lb",
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
            "id": "lb_config_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the specific configuration topic that you need help with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Dual NIC configuration (IPv4 and IPv6) for the backend instances",
                    "text": "Dual NIC configuration (IPv4 and IPv6) for the backend instances"
                },
                {
                    "value": "Health Probe",
                    "text": "Health Probe"
                },
                {
                    "value": "Load Balancer or NAT Rule",
                    "text": "Load Balancer or NAT Rule"
                },
                {
                    "value": "Health Probe",
                    "text": "Health Probe"
                },
                {
                    "value": "Backend Pool",
                    "text": "Backend Pool"
                },
                {
                    "value": "Frontend IP Addresses",
                    "text": "Frontend IP Addresses"
                },
                {
                    "value": "Floating IP",
                    "text": "Floating IP"
                },
                {
                    "value": "Availability Set",
                    "text": "Availability Set"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Topic not listed"
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
