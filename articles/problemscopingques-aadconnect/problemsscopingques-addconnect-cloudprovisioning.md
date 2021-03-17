<properties
    pageTitle="Cloud Provisioning (AD to AAD sync) job analysis"
    description="Cloud Provisioning (AD to AAD sync) job analysis"
    authors="dhanyahk"
    ms.author="dhanyahk"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32780785,32780786,32780787,32780788"
    productPesIds="16666"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemsscopingques-addconnect-cloudprovisioning.md"
    ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# PREVIEW: Provisioning job analysis
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "PREVIEW: Cloud Provisioning (AD to AAD sync) job analysis",
    "fileAttachmentHint": "Upload the trace or advanced verbose logging (if you have it enabled) from your corresponding AD domain machine. Learn <a href='https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#log-files'>more</a>",
        "diagnosticCard": {
        "title": "PREVIEW: Provisioning job analysis",
        "description": "Our self-service troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "We did not find a match for your specific problem in our knowledge base. See links below for other info that may address your problem."
    },
    "formElements": [
        {
            "id": "jobIdentifier",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Job ID (Unique identifier for your provisioning job, found in the 'Status' column of configuration grid view.):",
            "watermarkText": "Example: AD2AADProvisioning.c5357aa6263a46c8b990a7c935e24722.dcec0328-273b-4c51-9edb-5e22f2ae12c0",
            "infoBalloonText": "Unique identifier for your provisioning job, found in the 'Status' column of configuration grid view. You have a Job Id for both provisioning scope and Password Hash Sync.Please indicate which one you are providing.",
            "required": false,
            "numberOfLines": 4,
            "diagnosticInputRequiredClients": "Portal"
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
            "id": "userNameOrId",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "User(s) and / or group(s) impacted:",
            "watermarkText": "Example: foo@contosocom; fa93f620-091d-46b4-8edd-83195c62d746 (UPN; ObjectId)",
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
        },
        {
            "id": "CPLogs_useful",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Did Provisioning logs help with this issue?:",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "Yes"
                }, {
                    "value": "no",
                    "text": "No"
                }
            ],
            "required": false
        },

        {
            "id": "provisioning_logs_feedback",
            "order": 8,
            "controlType": "dropdown",
            "visibility": "CPLogs_useful == no",
            "displayLabel": "Provisioning logs feedback",
            "dropdownOptions": [
                {
                    "value": "Logs are missing",
                    "text": "Logs are missing"
                },
                {
                    "value": "Logs are available and unclear",
                    "text": "Logs are available and unclear"
                },
                {
                    "value": "Not applicable to support case",
                    "text": "Not applicable to support case"
                }
            ],
            "infoBalloonText": "We would love your feedback on how useful the logs are for troubleshooting.",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
