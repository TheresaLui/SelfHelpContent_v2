<properties
    pageTitle="Azure Media Services quota change encoding media reserved units"
    description="Azure Media Services quota change encoding media reserved units"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632090"
    productPesIds="14885"
    articleId="problemscopingques-quota-encoding-mru"
    cloudEnvironments="public"
    schemaVersion="1"
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
            "displayLabel": "When do you need the media reserved unit quota change by?",
            "required": true
        },
        {
            "id": "quota_MRU",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you requesting an increase in Media Reserved Units (MRUs) which are needed for processing files?",
            "watermarkText": "Select Yes or No",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "quota_MRU_one_selected",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you set your account ot have at least one unit of the desired Media Reserved Unit Type. Please set account to at least one RU before continuing with support ticket.",
            "infoBalloonText": "Please set account to at least one RU before continuing with support ticket",
            "visibilty": "quota_MRU == Yes",
            "watermarkText": "Select Yes or No",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "quota_MRU_one_selected_yes",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the new desired upper limit for MRUs (for example, default limit for S3 units is 10 in the Azure Portal and you may need to go up to 100?)",
            "infoBalloonText": "Please provide the max number of MRUs that you would need.",
            "visibilty": "quota_MRU == Yes",
            "watermarkText": "Select Yes or No",
            "dropdownOptions": [
                {
                    "value": "20",
                    "text": "20"
                },
                {
                    "value": "40",
                    "text": "40"
                },
                {
                    "value": "60",
                    "text": "60"
                },
                {
                    "value": "80",
                    "text": "80"
                },
                {
                    "value": "100",
                    "text": "100"
                },
                {
                    "value": "150",
                    "text": "150"
                },
                {
                    "value": "200+",
                    "text": "> 200"
                }
            ],
            "required": false
        },
        {
            "id": "quota_MRU_one_selected_yes",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the time period that you would need the increased quota held for?",
            "infoBalloonText": "Large quota increases should be explained in terms of time period that they will be needed for. Provide as much detail as possible up front to speed up the request.",
            "visibilty": "quota_MRU_one_selected_yes == 200+",
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
            "id": "quota_MRU_video_or_analytics",
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "Do you intend to use the quota increase for Encoding, Video Analytics or Audio Analytics",
            "infoBalloonText": "Please selected the use case desired for the quota increase",
            "visibilty": "quota_MRU == Yes",
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
            "id": "quota_MRU_hard_date",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When is the exact date that you require the quota to be available by?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Quota increase details",
            "watermarkText": "Provide additional details about your quota increase request, scenario, timeline, etc. that would be helpful for the support team when evaluating your request",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
