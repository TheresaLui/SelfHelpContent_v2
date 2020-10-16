<properties
	pageTitle="Performance and Throughput/Search queries are consistently slow"
	description="Search queries are consistently slow"
	authors="luisca"
	ms.author="luisca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681384"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="c04df8a8-ae43-4f13-8397-f1eda8c26484"
	ownershipId="AzureSearch_AzureSearch"
/>
# Search queries are consistently slow
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Search queries are consistently slow",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details. If possible, provide examples of queries that are slow",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "query_delay_cause",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "In what situation do you see delays?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "complex queries",
                    "text": "When issuing complex queries"
                },
                {
                    "value": "query volume",
                    "text": "When query volume increases"
                },
                {
                    "value": "field selected",
                    "text": "When too many fields are selected"
                },
                {
                    "value": "nothing usual",
                    "text": "No unusual reason, service simply degraded"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "tried_additional_replicas",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Have you tried adding additional replicas?",
            "controlType": "dropdown",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "true",
                    "text": "yes"
                },
                {
                    "value": "false",
                    "text": "no"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did you start seeing the issue?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---