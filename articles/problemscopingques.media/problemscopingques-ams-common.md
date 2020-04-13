<properties
    pageTitle="Azure Media Services common questions"
    description="Azure Media Services common questions"
    authors="akucer"
    ms.author="akucer"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632122, 32632093, 32632098, 32632110, 32632078, 32632089, 32632115, 32632113, 32632095, 32632130, 32632076, 32632112, 32632097, 32632088, 32632104, 32632118, 32729543, 32729544, 32729545, 32729547, 32729549, 32632079, 32729551, 32632127, 32632101"
    productPesIds="14885"
    articleId="problemscopingques-ams-common"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Services common questions for support
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
