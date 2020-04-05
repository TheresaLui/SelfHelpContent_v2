<properties
    pageTitle="Video Indexer common questions for support"
    description="Video Indexer common questions for support"
    ms.author="t-reutam"
    authors="ReutAmior"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32606552, 32606554, 32606567, 32606556, 32606569, 32606562, 32606555, 32606559, 32606558, 32606572, 32606551, 32606553, 32606557, 32606564, 32606566, 32606568, 32606570, 32606573, 32606560, 32606565"
    productPesIds="16535"
    articleId="problemscopingques-video-indexer"
    cloudEnvironments="public,blackForest,fairfax,mooncake"
    schemaVersion="1"
    ownershipId="StorageMediaEdge_Media_VI"
/>
# Video Indexer common questions for support
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Video Indexer common questions for support",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the issue begin?",
            "required": true
        },
        {
            "id": "problem_ongoing",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you still experiencing the issue?",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
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
            "id": "problem_end_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the issue stop?",
            "visibility": "problem_ongoing == no",
            "required": false
        },
        {
            "id": "region",
            "order": 4,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "You can find your account location in the Video Indexer portal under the Settings page in the Account tab",
            "displayLabel": "Please select the account region",
            "watermarkText": "Select the account region",
            "dropdownOptions": [
                {
                    "value": "Trial",
                    "text": "Trial"
                },
                {
                    "value": "East Asia",
                    "text": "East Asia"
                },
                {
                    "value": "Southeast Asia",
                    "text": "Southeast Asia"
                },
                {
                    "value": "Australia East",
                    "text": "Australia East"
                },
                {
                    "value": "North Europe",
                    "text": "North Europe"
                },
                {
                    "value": "West Europe",
                    "text": "West Europe"
                },
                {
                    "value": "Japan East",
                    "text": "Japan East"
                },
                {
                    "value": "UK South",
                    "text": "UK South"
                },
                {
                    "value": "East US",
                    "text": "East US"
                },
                {
                    "value": "East US 2",
                    "text": "East US 2"
                },
                {
                    "value": "South Central US",
                    "text": "South Central US"
                },
                {
                    "value": "West US",
                    "text": "West US"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "vi_account_id",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your Video Indexer account ID?",
            "watermarkText": "Please provide the Video Indexer account ID.",
            "infoBalloonText": "You can find your account ID in the Video Indexer portal under the Settings page in the Account tab",
            "required": true
        },
        {
            "id": "azure_subscription_id",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your Azure subscription ID?",
            "watermarkText": "Please provide the Azure subscription ID.",
            "infoBalloonText": "You can find the subscription ID in the Azure Portal.",
            "required": false
        },
        {
            "id": "trace_id",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the trace ID?",
            "watermarkText": "Please provide a trace ID (if you have one).",
            "required": false
        },
{
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide details about the scenario and issues that you ran into with the Video Indexer. Be sure to note if this worked previously and suddenly stopped working."
                }
            ]
        }
    ]
}
---
