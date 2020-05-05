<properties
    pageTitle="Authoring a custom policy definition"
    description="Authoring a custom policy definition"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32739640"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="d7371e4f-39e0-477f-a401-9af1173bc0a0"
    schemaVersion="1"
    ownershipId="Compute_AzurePolicy"
/>
# Authoring a custom policy definition
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Policy definition",
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
            "id": "rawPolicyDefinition",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the draft policy definition",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 30,
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