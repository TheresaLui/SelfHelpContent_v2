<properties
    pageTitle="PREVIEW: Get help from our intelligent knowledge base"
    description="Get help from our intelligent knowledge base"
    authors="hsku"
    ms.author="hsku"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689664,32689665,32689666,32689668"
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="8690704c-8c50-4703-b2f4-9f304954a550"
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
        "title": "PREVIEW: Get help from our intelligent knowledge base",
        "description": "Our self-service troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "We did not find a match for your specific problem in our knowledge base. See links below for other info that may address your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "userInput",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What task do you need to accomplish?",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        }
    ],
    "$schema": "SelfHelpContent"
}
---