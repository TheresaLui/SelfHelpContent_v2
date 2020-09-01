<properties 
    pageTitle="Problem with AAD B2C policy management"
    description="aadb2cpolicymanagement"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633316,32633317,32633318,32633320,32633325,32633327,32633328"
    productPesIds="16580"
    authors="parakhj"
    ms.author="parja"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="bbc964b0-abd5-454c-a3d6-166efb09c09a"
    	ownershipId="AzureIdentity_B2C"
/>
# Problem with AAD B2C policy management 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD B2C policy management",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "isCustomPolicy",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you using a built-in policy (for example: Sign-up or Sign-in Policy) or a custom policy?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Built-in Policy",
                    "value": "built-in"
                },
                {
                    "text": "Custom Policy",
                    "value": "custom"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "policyURL",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the 'Run Now' URL of the policy that you are using",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "correlationId",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Correlation ID",
            "content": null,
            "watermarkText": "Enter the correlation ID if one was shown when a user attempted to sign in",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Examples: error message in the Azure portal, error message on signing in, incorrect data on policy properties page",
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
            "visibility": null,
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---