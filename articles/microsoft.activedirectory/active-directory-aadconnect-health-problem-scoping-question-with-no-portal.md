<properties
    pageTitle="Scoping questions for AAD Connect"
    description="Scoping questions for AAD Connect"
    authors="rachundi"
    ms.author="rachundi"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32689664,32689665,32689666,32689668,32684522,32684507,32684508,32684512,32684521"
    productPesIds="16666"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="072411aa-a26c-492d-8399-05bb98639bae"
    ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Scoping questions for AAD Connect
---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "PREVIEW: Get help from our intelligent knowledge base",
    "fileAttachmentHint": null,
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
        }
    ],
    "$schema": "SelfHelpContent"
}
---