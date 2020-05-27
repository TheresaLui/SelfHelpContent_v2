<properties
    pageTitle="Configure a Load Balancer"
    description="Configure a Load Balancer"
    authors="ramandhillon84"
    ms.author="rdhillon"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32588972"
    productPesIds="16098"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="700961cc-d014-4545-be70-2069dc2e00ff"
	ownershipId="CloudNet_LoadBalancer"
/>

# SLB - Configure a Load Balancer 
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Configure a Load Balancer",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "config_lb",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the type of Load Balancer that you need configuration support for",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Load Balancer",
                    "text": "Azure Load Balancer"
                },
                {
                    "value": "A supported vendor product",
                    "text": "A supported vendor product"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "config_lb_sku",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the Load Balancer SKU that you need help with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Basic SKU",
                    "text": "Basic SKU"
                },
                {
                    "value": "Standard SKU",
                    "text": "Standard SKU"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "config_lb_type",
            "order": 3,
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
                }
            ],
            "required": false
        },
        {
            "id": "config_lb_ipaddress_family",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please select the Load Balancer IP address family",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "IPv4 Load Balancer",
                    "text": "IPv4 Load Balancer"
                },
                {
                    "value": "IPv6 Load Balancer",
                    "text": "IPv6 Load Balancer"
                }
            ],
            "required": false
        },
        {
            "id": "config_lb_zone",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Please select the Load Balancer fault-tolerence scope",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Zone-specific / zonal Load Balancer",
                    "text": "Zone-specific / zonal Load Balancer"
                },
                {
                    "value": "Zone redundant Load Balancer",
                    "text": "Zone redundant Load Balancer"
                }
            ],
            "required": false
        },
        {
            "id": "lb_config_type",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Please select the specific configuration topic that you need help with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
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
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
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
