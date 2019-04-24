<properties
    pageTitle="Azure Media Services quota change for Live Events or Channels"
    description="Azure Media Services quota change for Live Events or Channels"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632084"
    productPesIds="14885"
    articleId="problemscopingques-quota-streaming-liveevent-channels"
    cloudEnvironments="public"
    schemaVersion="1"
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
            "required": true
        },
        {
            "id": "quota_liveevent_increase",
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
                    "value": "30",
                    "text": "30"
                },
                {
                    "value": "40",
                    "text": "40"
                },
                {
                    "value": "50",
                    "text": "50"
                },
                {
                    "value": "75",
                    "text": "75"
                },
                {
                    "value": "100+",
                    "text": "> 100"
                }
            ],
            "required": true
        },
        {
            "id": "quota_liveevent_duration",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the time period that you would need the increased quota for?",
            "infoBalloonText": "Large quota increases should be explained in terms of time period that they will be needed for. Provide as much detail as possible up front to speed up the request.",
            "watermarkText": "Select one of the time periods",
            "dropdownOptions": [
                {
                    "value": "A few weeks",
                    "text": "A few weeks"
                },
                {
                    "value": "1 month",
                    "text": "1 month"
                },
                {
                    "value": "3 months",
                    "text": "3 months"
                },
                {
                    "value": "6 months",
                    "text": "6 months"
                },
                {
                    "value": "1 year",
                    "text": "1 year"
                },
                {
                    "value": "Indefinitely",
                    "text": "Indefinitely"
                },
                {
                    "value": "Dont know",
                    "text": "Dont know at this time"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Quota increase details",
            "watermarkText": "Provide additional details about your quota increase request, scenario, timeline, etc. that would be helpful for the support team when evaluating your request",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
