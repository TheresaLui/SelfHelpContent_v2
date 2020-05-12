<properties
    pageTitle="Secure Virtual Hub Management"
    description="Secure Virtual Hub Management"
    authors="TobyTu"
    ms.author="mariliu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32690527"
    productPesIds="16922"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="710961cc-a054-4550-be70-2069dc2e00ff"
	ownershipId="CloudNet_AzureFirewallManager"
/>
# Question about secure Virtual Hub Management
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Secure Virtual Hub Management",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "azure_firewall",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this about Azure Firewall Management using Azure Firewall Manager?",
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
            "id": "virtual_hub",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is Azure Firewall deployed in a Secured Virtual Hub?",
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
            "id": "partner_integration",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this about a Trusted Security Partner integration with Azure Firewall Manager?",
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
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
