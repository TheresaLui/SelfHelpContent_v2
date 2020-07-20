<properties
    pageTitle="Operation blocked by Policy"
    description="Operation blocked by Policy"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32739637,32739636"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="63c484a5-5a15-42d5-879c-91760b2051e6"
    schemaVersion="1"
    ownershipId="Compute_AzurePolicy"
/>
# Operation blocked by Policy
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Error message",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "correlationId",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "Please provide the correlation Id",
            "required": false
        },
        {
            "id": "errorMessage",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error message",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 40,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about the issue and what is your expectation",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
