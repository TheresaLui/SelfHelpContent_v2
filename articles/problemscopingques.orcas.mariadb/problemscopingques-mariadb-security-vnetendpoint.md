<properties
    pageTitle="Security"
    description="Security"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640160"
    productPesIds="16617"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-mariadb-security-vnet_endpoint"
/>
# Security - VNET service endpoints
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Security VNET Service Endpoints",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "server_vnet_subscription",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are your server and VNet under same subscription?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "resource_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your VNet resource ID?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
