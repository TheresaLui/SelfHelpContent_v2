<properties
    pageTitle="PREVIEW: Get help from our intelligent knowledge base"
    description="Get help from our intelligent knowledge base"
    authors="hsku"
    ms.author="hsku"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689667"
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="99583156-6f45-421d-beb7-4484967c149a"
    ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# PREVIEW: Get help from our Virtual Assistant
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "PREVIEW: Get help from our intelligent knowledge base",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "PREVIEW: Provisioning job analysis",
        "description": "Our self-service troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "We did not find a match for your specific problem in our knowledge base. See links below for other info that may address your problem."
    },
    "formElements": [
        {
            "id": "whichUser",
            "visibility": null,
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which user is experiencing this problem?",
            "content": null,
            "watermarkText": "Enter user name or Object ID of the user in Azure Active Directory",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "resource",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Which Resource ID is experiencing this problem?",
            "content": null,
            "watermarkText": "Note: Resource ID information can be found in the properties blade of your domain service",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "jobIdentifier",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Job ID (Unique identifier for your provisioning job, found in the progress bar):",
            "watermarkText": "Example: serviceNow.5547032d9415500cb27b277e3fb6f2c8.5aaf8326-b305-4b63-aa55-0990eb3265f5",
            "infoBalloonText": "Unique identifier for your provisioning job, found in the progress bar.",
            "required": false,
            "numberOfLines": 4,
            "diagnosticInputRequiredClients": "Portal"
        }
    ],
    "$schema": "SelfHelpContent"
}
---