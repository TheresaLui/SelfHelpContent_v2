<properties
	pageTitle="Performance and Throughput/Some search requests are throttled (Response code 503)"
	description="Some search requests are throttled (Response code 503)"
	authors="luisca"
	ms.author="luisca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681387"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="ba6ca253-818d-48ae-b386-428a8ad8a4f5"
	ownershipId="AzureSearch_AzureSearch"
/>
# Some search requests are throttled (Response code 503)
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Some search requests are throttled (Response code 503)",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details. If possible, describe the indexing load, and the symptoms.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "indexing_throughput_previously_tested",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you tried a similar indexing throughput in the past?",
            "controlType": "dropdown",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "true",
                    "text": "yes, this workload usually works"
                },
                {
                    "value": "false",
                    "text": "no, this is the first time we try this indexing throughput"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "tried_additional_replicas_or_partitions",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Have you tried adding additional replicas or partitions to mitigate the problem?",
            "controlType": "dropdown",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "replicas",
                    "text": "Yes, tried adding more replicas"
                },
                {
                    "value": "partitions",
                    "text": "Yes, tried adding more partitions"
                },
                {
                    "value": "no",
                    "text": "No, I have not modified the service configuration"
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