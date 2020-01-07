<properties
    pageTitle="Uploading a video to Video Indexer"
    description="Uploading a video to Video Indexer"
    authors="ReutAmior"
    ms.author="ReutAmior"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32606571"
    productPesIds="16535"
    articleId="problemscopingques-video-indexer-upload"
    cloudEnvironments="public"
    schemaVersion="1"
/>
# Uploading a video to Video Indexer
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Uploading a video to Video Indexer",
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
            }
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the issue begin?",
            "visibility": "problem_ongoing == no",
            "required": false
        },
        {
            "id": "region",
            "order": 4,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "You can find the account location in the Video Indexer portal under Settings->Account->Account region",
            "displayLabel": "Please select the Account region",
            "watermarkText": "Select the Account region",
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
                    "text": "Mozilla Firefox 42 or higher"
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
            "displayLabel": "What is your Video Indexer Account ID?",
            "watermarkText": "Please provide the Video Indexer account ID.",
            "infoBalloonText": "You can find your account ID in the Video Indexer portal under Settings->Account->Account ID",
            "required": true
        },
        {
            "id": "azure_subscription_id",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your Azure Subscription ID?",
            "watermarkText": "Please provide the Azure Subscription ID.",
            "infoBalloonText": "You can find the subscription ID in the Azure Portal.",
            "required": false
        },
        {
            "id": "video_id",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your Video ID?",
            "watermarkText": "Please provide the video ID.",
            "required": true
        },
        {
            "id": "public",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Is your video public?",
            "watermarkText": "Please mark if your video is publicly shared.",
            "infoBalloonText": "In order to check the video upload issue, the support team needs access to the video or the file itself.",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
            }
            "required": true
        },
        {
            "id": "trace_id",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Trace ID?",
            "watermarkText": "Please provide a Trace ID (if you have one).",
            "required": false
        },
{
            "id": "problem_description", //This is a required value
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
            "hints": [
                {
                    "text": "Please provide more details about the issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
