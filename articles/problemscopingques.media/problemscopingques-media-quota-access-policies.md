<properties
    pageTitle="Azure Media Services quota change for Access Polices"
    description="Azure Media Services quota change for  Access Polices"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632075"
    productPesIds="14885"
    articleId="problemscopingques-quota-access-policies"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Services common questions for quota changes for Access Policies
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Services Access or Streaming Policies",
    "fileAttachmentHint": "Please attach any details on your quota request, including planned ramp-up, regional quota required, and your overall schedule for any complex or multi-month quota requests",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What date do you need the Access or Streaming Policy quota changed by?",
            "required": true
        },
        {
            "id": "quota_accesspolicy_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of policy do you need increased?",
            "watermarkText": "Select a policy type for quota increase",
            "dropdownOptions": [
                {
                    "value": "Access Policy",
                    "text": "Access Policy (v2 API)"
                },
                {
                    "value": "Streaming Policy",
                    "text": "Streaming Policy (v3 API)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "quota_accesspolicy_increase",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How many Access or Streaming Polices do you need?",
            "watermarkText": "Enter a value",
            "required": true
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
