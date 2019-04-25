<properties
    pageTitle="Azure Media Services quota change for Assets"
    description="Azure Media Services quota change for Assets"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632080"
    productPesIds="14885"
    articleId="problemscopingques-quota-assets"
    cloudEnvironments="public"
    schemaVersion="1"
/>
# Azure Media Services common questions for quota changes for Assets
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Services Assets quota increase",
    "fileAttachmentHint": "Please attach any detail documents for your quota request, including planned monthly ramp-up, regional quota requirements, etc. ",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What date do you need the Asset quota increase changed by?",
            "required": true
        },
        {
            "id": "quota_assets_increase",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Approximately how many total Assets do you need for your account?",
            "watermarkText": "Select a value",
            "dropdownOptions": [
                {
                    "value": "1 Million",
                    "text": "1 Million (this is default quota)"
                },
                {
                    "value": "2 Million",
                    "text": "2 Million"
                },
                {
                    "value": "4 Million",
                    "text": "4 Million"
                },
                {
                    "value": "5-10 Million",
                    "text": "5 to 10 Million"
                }
            ],
            "required": false
        },
        {
            "id": "quota_assets_duration",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the time period that you would need the increased quota for?",
            "infoBalloonText": "Large quota increases should be explained in terms of time period that they will be needed for. Provide as much detail as possible up front to speed up the request.",
            "watermarkText": "Select one of the time periods",
            "dropdownOptions": [
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
                    "value": "2 years",
                    "text": "2 years"
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
