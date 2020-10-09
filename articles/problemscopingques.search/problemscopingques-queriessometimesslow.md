<properties
	pageTitle="Performance and Throughput/Search queries are sometimes slow"
	description="Search queries are sometimes slow"
	authors="luisca"
	ms.author="luisca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681385"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="ffb7f897-bdab-45dc-a967-c1ce5b8cc5bc"
	ownershipId="AzureSearch_AzureSearch"
/>
# Search queries are sometimes slow
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Search queries are sometimes slow",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the issue. Please provide examples of queries that are slow",
            "required": false,
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
            "id": "Have you tried adding additional replicas?",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Have you tried adding additional replicas?",
            "required": true
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