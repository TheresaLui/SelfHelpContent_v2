<properties
    pageTitle="Azure Media Services quota change encoding media reserved units"
    description="Azure Media Services quota change encoding media reserved units"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632090"
    productPesIds="14885"
    articleId="problemscopingques-quota-encoding-mru"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Services common questions for Quota changes encoding media reserved units
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Services encoding media reserved unit quota request",
    "fileAttachmentHint": "Please attach any details on your quota request, including planned ramp-up, regional quota required, and your overall schedule for any complex or multi-month quota requests",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What date do you need the Media Reserved Unit quota increase by?",
            "required": true
        },
        {
            "id": "quota_MRU_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which type of Media Reserved Units (MRU) do you need?",
            "infoBalloonText": "For details on Media Reserved Unit types please see <a href='https://docs.microsoft.com/azure/media-services/previous/media-services-scale-media-processing-overview#choosing-between-different-reserved-unit-types'>documentation on reserved unit types </a>",
            "watermarkText": "Select one of the Media Reserved Unit types",
            "dropdownOptions": [
                {
                    "value": "S1",
                    "text": "S1"
                },
                {
                    "value": "S2",
                    "text": "S2"
                },
                {
                    "value": "S3",
                    "text": "S3"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "quota_MRU_value",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the new desired upper limit for Media Reserved Units (MRU) (for example, the default limit for S3 units is 10 in the Azure Portal and you may need to go up to 100)",
            "infoBalloonText": "Please provide the max number of Media Reserved Units (MRU) that you would need.",
            "watermarkText": "Select a value",
            "dropdownOptions": [
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
                    "value": "60",
                    "text": "60"
                },
                {
                    "value": "70",
                    "text": "70"
                },
                {
                    "value": "80",
                    "text": "80"
                },
                {
                    "value": "90",
                    "text": "90"
                },
                {
                    "value": "100",
                    "text": "100"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "quota_MRU_200_plus_details",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the new requested upper limit for Media Reserved Units (MRU)?",
            "infoBalloonText": "Please provide the max upper limit of Media Reserved Units (MRU) that you  need.",
            "watermarkText": "Enter a numeric value",
            "visibility": "quota_MRU_value == Other",
            "required": false
        },
        {
            "id": "quota_MRU_time_period",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the time period that you require the increased quota held for?",
            "infoBalloonText": "Large quota increases should be explained in terms of time period that they will be required to be held for. Provide as much detail as possible up front to speed up the request.",
            "visibility": "quota_MRU_value == Other",
            "watermarkText": "Select a time period",
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
            "id": "quota_MRU_video_or_analytics",
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "Do you intend to use the quota increase for Encoding, Video Analytics or Audio Analytics",
            "infoBalloonText": "Please select the use case desired for the quota increase",
            "watermarkText": "Select one or more of the use cases",
            "dropdownOptions": [
                {
                    "value": "Encoding Audio",
                    "text": "Encoding Audio"
                },
                {
                    "value": "Encoding Video",
                    "text": "Encoding Video"
                },
                {
                    "value": "Audio Analytics",
                    "text": "Audio Analytics"
                },
                {
                    "value": "Video Analytics",
                    "text": "Video Analytics"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
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
