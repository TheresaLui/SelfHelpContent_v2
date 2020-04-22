<properties
    pageTitle="Azure Media Services quota change for Live Events or Channels"
    description="Azure Media Services quota change for Live Events or Channels"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632084"
    productPesIds="14885"
    articleId="problemscopingques-quota-streaming-liveevent-channels"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Services common questions for quota changes for LiveEvents or Channels
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Services Live Events (v3) or Channels (v2)",
    "fileAttachmentHint": "Please attach any details on your quota request, including planned ramp-up, regional quota required, and your overall schedule for any complex or multi-month quota requests",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What date do you need the Live Event or Channel quota changed by?",
            "required": true
        },
        {
            "id": "quota_liveevent",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "What type of LiveEvent or Channel are you requesting an increase for?",
            "watermarkText": "Select one or multiple of the following types",
            "dropdownOptions": [
                {
                    "value": "Pass-through",
                    "text": "Pass-through"
                },
                {
                    "value": "Live Encoding - Standard 720p30",
                    "text": "Live Encoding - Standard 720p30"
                },
                {
                    "value": "Live Encoding - Premium 1080p30",
                    "text": "Live Encoding - Premium 1080p30"
                }
            ],
            "required": false
        },
        {
            "id": "quota_liveevent_value",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How many concurrent LiveEvents or Channels do you need?",
            "infoBalloonText": "Please set the maximum concurrent number of Live Events needed. See the documentation <a href='https://docs.microsoft.com/azure/media-services/latest/live-streaming-overview'>Live Events in v3 API </a> for details.",
            "watermarkText": "Select a value",
            "dropdownOptions": [
                {
                    "value": "5",
                    "text": "5 (this is default quota)"
                },
                {
                    "value": "10",
                    "text": "10"
                },
                {
                    "value": "15",
                    "text": "15"
                },
                {
                    "value": "20",
                    "text": "20"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "quota_liveevent_Other_value",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the new requested upper limit for Live Events or Channels?",
            "infoBalloonText": "Please provide the max upper limit of Live Events or Channels that you need.",
            "watermarkText": "Enter a numeric value",
            "visibility": "quota_liveevent_value == Other",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Quota increase details",
            "watermarkText": "Provide additional details about your quota increase request, scenario, timeline, etc. that would be helpful for the support team when evaluating your request",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
