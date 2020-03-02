<properties
    pageTitle="Permission error message from Policy"
    description="Permission error message from Policy"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32636049"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="public, Fairfax"
    articleId="63c484a5-5a15-42d5-879c-91760b2051e6"
    schemaVersion="1"
	ownershipId="Compute_AzurePolicy"
/>
#Permission error message from Policy
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
            "id": "errorMessage",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the error message",
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