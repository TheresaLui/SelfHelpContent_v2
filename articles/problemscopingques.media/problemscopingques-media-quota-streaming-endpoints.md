<properties
    pageTitle="Azure Media Services quota change for Packager and Streaming Endpoints"
    description="Azure Media Services  quota change for Packager and Streaming Endpoints"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632123"
    productPesIds="14885"
    articleId="problemscopingques-quota-streaming-endpoints"
    cloudEnvironments="public"
    schemaVersion="1"
/>
# Azure Media Services common questions for quota changes for Streaming Endpoints
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Services Premium Streaming Endpoint (Packager) reserved unit quota request",
    "fileAttachmentHint": "Please attach any details on your quota request, including planned ramp-up, regional quota required, and your overall schedule for any complex or multi-month quota requests",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When do you need the Premium Streaming Endpoint (Packager) unit quota changed by?",
            "required": true
        },
        {
            "id": "quota_SRU",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you requesting an increase in Premium Streaming Endpoints to hit a specific egress limit?",
            "watermarkText": "Select Yes or No",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "quota_SRU_increase",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How many Premium Streaming Endpoint units do you need?",
            "infoBalloonText": "Please set the number of Streaming endpoint units needed based on a calculation of your max egress in units of 200 Mbps. There is a max of 2 Streaming Endpoints allowed per account, but units can be increased in increments. See the documentation <a href='https://docs.microsoft.com/azure/media-services/latest/streaming-endpoint-concept'>Streaming Endpoints </a> for details.",
            "watermarkText": "Select a value",
            "dropdownOptions": [
                {
                    "value": "5",
                    "text": "5"
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
                    "text": "more than 100"
                }
            ],
            "required": false
        },
        {
            "id": "quota_SRU_duration",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the time period that you would need the increased quota held for?",
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
