<properties
    pageTitle="Azure Media Services quota change for Assets"
    description="Azure Media Services quota change for Assets"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632080"
    productPesIds="14885"
    articleId="problemscopingques-quota-assets"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
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
            "controlType": "textbox",
            "displayLabel": "Approximately how many total Assets do you need for your account? The default quota is 1 Million Assets.",
            "watermarkText": "Please enter a value for max Assets",
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
    ],
    "$schema": "SelfHelpContent"
}
---
