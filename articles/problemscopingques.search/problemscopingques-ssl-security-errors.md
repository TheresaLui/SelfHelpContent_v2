<properties
	pageTitle="SSL or other security errors"
	description="SSL or other security errors"
	authors="mcarter"
	ms.author="mcarter"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681388"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="bdfecc88-6339-4a52-a25e-ee16ee22cfde"
	ownershipId="AzureSearch_AzureSearch"
/>
# SSL or other security errors
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "SSL or other security errors",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the SSL or security issue you experienced",
            "useAsAdditionalDetails": true,
            "required": true,
	    "watermarkText":"Please provide the full error text when possible."
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last experience an SSL or security error?",
            "required": true
        },
        {
            "id": "ssl_cache",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you using an SSL certificate cache?",
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
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "client_used",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What client were you using to connect?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Search Explorer in Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "Custom client using the REST API",
                    "text": "Custom client using REST API"
                },
                {
                    "value": "Custom client using an SDK",
                    "text": "Custom client using an SDK"
                },
                {
                    "value": "Postman",
                    "text": "Postman"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": false
        },
        {
            "id": "ip_firewall",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do you have an IP firewall enabled on the search service?",
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
                    "text": "Don't Know"
                }
            ],
            "required": false
        },
        {
            "id": "private_mode",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Is your search service endoint public or private?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Public",
                    "text": "Public"
                },
                {
                    "value": "Private",
                    "text": "Private"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
