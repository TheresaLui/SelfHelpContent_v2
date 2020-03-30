<properties
    pageTitle="problem-with-redeeming-an-invitation"
    description="Problem with redeeming an invitation"
    authors="marialai"
    ms.author="mal"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615429"
    productPesIds="16578"
    cloudEnvironments="public, Fairfax, Mooncake"
    schemaVersion="1"
    articleId="problemscopingques-aadb2bredemptionissue"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>
# Problem with redeeming an invitation
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with redeeming an invitation",
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
            "displayLabel": "Who is experiencing a problem with redeeming an invitation?",
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
                    "text": "I have a different problem, not a redemption problem.",
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
            "displayLabel": "What is the email address on the invitation being redeemed?",
            "content": null,
            "watermarkText": "This is the email address the invitation email was sent to, which might be different from your email address.",
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
            "displayLabel": "Which directory or organization are you trying to redeem an invitation for?",
            "content": null,
            "watermarkText": "This is the organization that is sharing the resource.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whichApp",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where does this problem occur? ",
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
            "id": "errorText",
            "visibility": null,
            "order": 6,
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
            "order": 7,
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
            "order": 8,
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
            "order": 9,
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
