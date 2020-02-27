<properties
    pageTitle="Application Gateway configuration and setup"
    description="Application Gateway configuration and setup"
    authors="TobyTu"
    ms.author="mariliu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684007"
    productPesIds="15922"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="710961cc-d014-4550-be70-2069dc2e00ff"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Questions Application Gateway configuration and setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Application Gateway configuration and setup",
    "fileAttachmentHint": "Upload your YAML configuration file",
    "formElements": [
        {
            "id": "advance-networking",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have Advanced Networking enabled?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "azure-resource",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which Azure resource is your Application Gateway handling ingress traffic for?",
            "watermarkText": "Enter the name of the Azure resource(s)",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
