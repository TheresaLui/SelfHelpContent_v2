<properties
	articleId="problemscopingques-configuring-collection-of-metrics-or-sending-metrics-using-api-ai-sdk-rest-api-telegraf"
	pageTitle="Configuring collection of metrics or sending metrics using API-AI SDK, REST API, Telegraf"
	description="Configuring collection of metrics or sending metrics using API-AI SDK, REST API, Telegraf"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684770,32684771,32684769"
	productPesIds="16250"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>

# Configuring collection of metrics or sending metrics using API-AI SDK, REST API, Telegraf
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configuring collection of metrics or sending metrics using API-AI SDK, REST API, Telegraf",
    "fileAttachmentHint": "If applicable, please upload a screenshot of the error.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
        {
            "id": "problem_frequency",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How frequently does the problem occur?",
            "watermarkText": "How frequently does the problem occur?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Once",
                    "text": "Issue occurred once only"
                },
                {
                    "value": "Multiple",
                    "text": "Issue occurred more than once but not always"
                },
                {
                    "value": "Ongoing",
                    "text": "Issue occurs consistantly"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "api_call",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of the API call that is being used.",
            "watermarkText": "Provide details of the API call that is being used.",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the verbatim error message(s) you are receiving.",
            "watermarkText": "Provide the verbatim error message(s) you are receiving.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "If applicable, please attach a screenshot of the error."
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---