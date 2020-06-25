<properties
    pageTitle="Provisioning job analysis"
    description="Provisioning job analysis"
    authors="hsku"
    ms.author="hsku"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684504"
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="faf5d3af-1b90-47de-b3e9-be37ec140b10"
    ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# PREVIEW: Provisioning job analysis
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "PREVIEW: Provisioning job analysis",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "PREVIEW: Provisioning job analysis",
        "description": "Our self-service troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "We did not find a match for your specific problem in our knowledge base. See links below for other info that may address your problem."
    },
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Description Test 02",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "jobIdentifier",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Job ID",
            "watermarkText": "Unique identifier for your provisioning configuration, found in the view technical information section of the provisioning progress bar.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "userNameOrId",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "User Experiencing Problem:",
            "watermarkText": "Example: foo@contosocom; fa93f620-091d-46b4-8edd-83195c62d746 (UPN; ObjectId)",
            "required": false
        },
        {
            "id": "application_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Application name",
            "watermarkText": "Example: Salesforce, Contoso App",
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