<properties
	pageTitle="Performance and Throughput/Indexing throughput is lower than expected"
	description="Indexing throughput is lower than expected"
	authors="luisca"
	ms.author="luisca"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681351"
	productPesIds="15568"
	cloudEnvironments="Public,MoonCake,FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="023584a1-899d-46f9-8dd5-476775976500"
	ownershipId="AzureSearch_AzureSearch"
/>
# Indexing throughput is lower than expected
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Indexing throughput is lower than expected",
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
            "id": "data_source",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "How are you feeding data to the index?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "indexer",
                    "text": "Using an indexer"
                },
                {
                    "value": "push",
                    "text": "Pushing data directly into the index"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "indexing_throughput_previously_tested",
            "order": 3,
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
            "order": 4,
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
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did you start seeing the issue?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---