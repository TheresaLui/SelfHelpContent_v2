<properties
    pageTitle="problem-with-leaving-an-organization"
    description="Problem with leaving an organization"
    authors="marialai"
    ms.author="mal"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615392"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-aadb2bleavingissue"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>
# Problem with leaving an organization
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with leaving an organization",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 1,
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
            "id": "whoInviter",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Who is experiencing a problem with leaving an organization?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Me",
                    "value": "thisUser"
                },
                {
                    "text": "Another user. Enter UPN below.",
                    "value": "anotherUser"
                },
                {
                    "text": "I have a different problem, not a leaving problem.",
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
            "id": "whoInvited",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the email address of the user needing to leave an organization?",
            "content": null,
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
            "id": "whichOrg",
            "visibility": null,
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which organization is the user trying to leave?",
            "content": null,
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
            "id": "errorText",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Paste in the error text, including the correlation ID if any.",
            "content": null,
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
            "id": "URL",
            "visibility": null,
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the URL of the page you saw the problem on?",
            "content": null,
            "watermarkText": "Enter the URL you were trying to access when the error happened. Note that the error page itself may have a URL, that’s not the one we need.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "reproStepsText",
            "visibility": null,
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What specific steps did you or the user follow that resulted in the error?",
            "content": null,
            "watermarkText": "List each specific step taken, and where those steps were performed.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 10
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "You may provide additional details here",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---
