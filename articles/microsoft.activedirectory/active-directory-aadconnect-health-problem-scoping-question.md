<properties
    pageTitle="PREVIEW: Get help from our intelligent knowledge base"
    description="Get help from our intelligent knowledge base"
    authors="hsku"
    ms.author="hsku"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689664,32689665,32689666,32689668,32684522,32684507,32684508,32684512,32684521,32689667,32447390,32447391,32570967,32565593,32570965,32570966"
    productPesIds="16666,16576"
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
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "DescriptionTest",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "jobIdentifier",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Job ID",
            "watermarkText": "Example: serviceNow.5547032d9415500cb27b277e3fb6f2c8.5aaf8326-b305-4b63-aa55-0990eb3265f5",
            "infoBalloonText": "Unique identifier for your provisioning job, found in the progress bar.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "userNameOrId",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "User(s) and / or group(s) impacted:",
            "watermarkText": "Example: foo@contosocom; fa93f620-091d-46b4-8edd-83195c62d746 (UPN; ObjectId)",
            "required": false
        },
        {
            "id": "application_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Application name",
            "watermarkText": "Example: Salesforce, Workday",
            "required": false
        },
        {
            "id": "appId",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Application ID",
            "watermarkText": "Example: 751d4c55-15c1-4ed0-b2c0-ef30ebfe5743",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": false
        },
        {
            "id": "problem_steps_taken",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe the steps, if any, that you already took to remedy the issue",
            "watermarkText": "Example: Restarted provisioning before creating support case. Reviewed documentation.",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
