<properties
    pageTitle="Other problem with group"
    description="otherproblemgroup"
    authors="anupnadigm"
    ms.author="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32586794"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="3e0776b4-a7da-4b66-8018-2eee9634af9b"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Other problem with user or group

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Other problem with group",
    "fileAttachmentHint": "Screenshot of problem",
    "formElements": [
        {
            "id": "whoHavingProblem",
            "visibility": null,
            "order": 2,
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
                    "value": "dont_know_answer"
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
            "visibility": "whoHavingProblem==otherUser",
            "order": 3,
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
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Where does the problem occur?",
            "content": null,
            "watermarkText": "Example: Azure portal, PowerShell, a Microsoft or third-party application (identify which one)",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
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
            "id": "problem_start_time",
            "visibility": null,
            "order": 6,
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
            "order": 7,
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
