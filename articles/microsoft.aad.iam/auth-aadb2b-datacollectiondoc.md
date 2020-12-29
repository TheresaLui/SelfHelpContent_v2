<properties
    pageTitle="problem-with-collab-settings"
    description="Problem with external collaboration settings"
    authors="marialai"
    ms.author="mal"
    selfHelpType="problemScopingQuestions"
    supportTopicIds=""
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-aadb2bsettingsissue"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>
# Problem with external collaboration settings
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with external collaboration settings",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "Problem with Azure Active Directory B2B Guest users",
        "description": "Please enter the following data for the self-service troubleshooter to assist in resolving your issue. Data can be retrieved from the Error Message or from the Azure Active Directory Sign-ins Blade:",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your inputs."
    },
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
            "displayLabel": "Who is experiencing a problem with external collaboration settings?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Me",
                    "value": "thisUser"
                },
                {
                    "text": "Another user. Enter UPN in additional details field",
                    "value": "anotherUser"
                },
                {
                    "text": "I have a different problem, not a settings problem.",
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
            "id": "howHelp",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I need help with:",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Getting instructions to accomplish a settings management task",
                    "value": "instructions"
                },{
                    "text": "Troubleshooting an error that occurred while I managed settings",
                    "value": "troubleshooting"
                },{
                    "text": "Other. Provide more details in text field.",
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
            "id": "whichApp",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Where does the problem occur? ",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "On this app (portal.azure.com)",
                    "value": "portal.azure.com"
                },
                {
                    "text": "MyApps, MyProfile, or MyAccess",
                    "value": "myStar"
                },
                {
                    "text": "Other Microsoft apps like PowerBI and Teams",
                    "value": "firstPartyApp"
                },
                {
                    "text": "Non-Microsoft app",
                    "value": "thirdPartyApp"
                },{
                    "text": "PowerShell",
                    "value": "powerShell"
                },{
                    "text": "B2B invitation manager API",
                    "value": "B2Bapi"
                },{
                    "text": "I don't know",
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
            "id": "problem_description",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Full Error Message:",
            "content": null,
            "watermarkText": "Example: AADSTS50076: Due to a configuration change made by your administrator...",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 3,
            "diagnosticInputRequiredClients": "Portal"
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
            "id": "resourceID",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Resoure ID",
            "watermarkText": "Provide Resource ID for Resource with issue",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
