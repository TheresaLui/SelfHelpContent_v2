<properties
    pageTitle="Azure Media Services quota change for Packager and Streaming Endpoints"
    description="Azure Media Services  quota change for Packager and Streaming Endpoints"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632123"
    productPesIds="14885"
    articleId="problemscopingques-quota-streaming-endpoints"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
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
            "id": "quota_SRU_value",
            "order": 2,
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
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "quota_SRU_Other_value",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the new requested upper limit for Premium Streaming Endpoint Units?",
            "infoBalloonText": "Please provide the max upper limit of Premium Streaming Endpoint Units that you  need.",
            "watermarkText": "Enter a numeric value",
            "visibility": "quota_SRU_value == Other",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
