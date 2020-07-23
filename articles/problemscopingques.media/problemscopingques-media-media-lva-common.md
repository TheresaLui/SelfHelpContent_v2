<properties
    pageTitle="Azure Media Services Live Video Analytics common questions"
    description="Azure Media Services Live Video Analytics common questions"
    authors="akucer"
    ms.author="akucer"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32740853,32740854,32740855,32740856"
    productPesIds="14885"
    articleId="problemscopingques-media-lva-common"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Services Live Video Analytics common questions for support
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Services common questions for support",
    "fileAttachmentHint": "Please provide screenshots showing the error or any relevant files",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the issue begin?",
            "required": true
        },
        {
            "id": "api_vs_portal",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Do you have an API or Azure portal issue?",
            "dropdownOptions": [
                {
                    "value": "API",
                    "text": "API"
                },
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "api_version",
            "order": 3,
            "visibility": "api_vs_portal == API",
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the Azure Media Services API version(s) where the issue occurred.",
            "watermarkText": "Choose multiple options",
            "dropdownOptions": [
                {
                    "value": "v2",
                    "text": "v2"
                },
                {
                    "value": "v3",
                    "text": "v3"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Scenario details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---