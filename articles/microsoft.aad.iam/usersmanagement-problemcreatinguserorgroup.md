<properties
    pageTitle="Problem creating a group"
    description="problemcreatinggroup"
    authors="anupnadigm"
    ms.author="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32586792"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="ea6a7744-1273-4571-b351-90f5938a0e51"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem creating a group

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem creating a group",
    "fileAttachmentHint": "Screenshot of problem",
    "formElements": [
        {
            "id": "notB2b",
            "visibility": null,
            "order": 2,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "If the problem has to do with inviting guest users to collaborate with your organization, please go to the previous step and select the category 'Adding a guest user(B2B)'.'",
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
            "id": "whichUser",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which user is experiencing the problem?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Me",
                    "value": "self"
                },
                {
                    "text": "Another user",
                    "value": "otherUser"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "other"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whichOtherUser",
            "visibility": "whichUser==otherUser",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the user name of the user who is having the problem?",
            "content": null,
            "watermarkText": "Enter user name (such as alice@contoso.com) or Object ID of the user in Azure Active Directory",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whereProblem",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where does the problem occur?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure portal",
                    "value": "azurePortal"
                },
                {
                    "text": "PowerShell",
                    "value": "powerShell"
                },
                {
                    "text": "Access panel",
                    "value": "accesPanel"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "other"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
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
            "watermarkText": "Examples: error message in the Azure portal, add button not enabled",
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
