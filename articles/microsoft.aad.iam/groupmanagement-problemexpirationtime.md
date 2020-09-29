<properties
    pageTitle="Group expiration"
    description="Group expiration"
    authors="someshc"
	ms.author="someshc"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615385"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="9907CFC4-FA80-474B-9A05-CB1C9056EF46"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Group expiration

---
{
    "resourceRequired": false,
    "title": "Group expiration",
    "fileAttachmentHint": "Screenshot of problem",
    "formElements": [
        {
            "id": "groupId",
            "visibility": null,
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Object ID of the group you are having problems with?",
            "content": null,
            "watermarkText": "The Object ID can be found by opening the group in the portal, in the Overview tab in the Essentials box on the very top.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "whichUser",
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
            "watermarkText": "Examples: steps followed, error message received, describe expected behavior",
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