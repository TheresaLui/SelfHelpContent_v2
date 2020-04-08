<properties 
    pageTitle="Problem with AAD B2C user management"
    description="aadb2cusermanagement"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633306,32633307,32633315,32633319,32633322"
    productPesIds="16580"
    authors="parakhj"
    ms.author="parja"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="95844536-f669-43e4-873c-5c1af6f4310d"
    	ownershipId="AzureIdentity_B2C"
/>
# Problem with AAD B2C user management 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD B2C user management",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whichUser",
            "visibility": null,
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which user is experiencing this problem?",
            "content": null,
            "watermarkText": "Enter username, object ID or UPN of the user",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "userCreationStyle",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How was the user added into the directory?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Via the Azure AD B2C 'Users and groups' menu",
                    "value": "IAM"
                },
                {
                    "text": "Through a sign-up process (via a policy)",
                    "value": "Policy"
                },
                {
                    "text": "Using the Graph API",
                    "value": "Graph"
                },
                {
                    "text": "Other or don't know",
                    "value": "Other"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "getUserRegistration",
            "visibility": "userCreationStyle==IAM",
            "order": 3,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Users created through the 'Users and groups' menu do not have the ability to sign in through a policy.",
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the user trying to accomplish?",
            "content": null,
            "watermarkText": "Examples: trying to sign in to an application, trying to manage Azure AD B2C settings.",
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
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Correlation ID",
            "content": null,
            "watermarkText": "Enter the correlation ID if one was shown",
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
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Examples: error message in the Azure portal, error message when signing in",
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
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem occur?",
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
            "order": 8,
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