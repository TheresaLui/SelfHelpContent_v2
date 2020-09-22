<properties
    pageTitle="PS, CLI or API Inquires or Issues"
    description="PS, CLI or API Inquires or Issues"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32739639"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="35be6cf2-fe16-44f7-97e4-693cfdf04491"
    schemaVersion="1"
    ownershipId="Compute_AzurePolicy"
/>
# PS, CLI or API Inquires or Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "PS, CLI or API Inquires or Issues",
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
            "id": "command",
            "order": 20,
            "controlType": "textbox",
            "displayLabel": "What is the Cmdlet/command/API being called?",
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