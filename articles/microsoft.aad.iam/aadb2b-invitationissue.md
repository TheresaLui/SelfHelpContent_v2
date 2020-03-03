<properties
    pageTitle="problem-with-inviting-an-external-user"
    description="Problem with inviting an external user" 
    authors="marialai" 
    ms.author="mal"
    selfHelpType="problemScopingQuestions" 
    supportTopicIds="32615387" 
    productPesIds="16578" 
    cloudEnvironments="public" 
    schemaVersion="1"
    articleId="problemscopingques-aadb2binvitationissue"
	ownershipId="AzureIdentity_B2B"
/>
# Problem with inviting an external user
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with inviting an external user",
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
            "displayLabel": "Who is trying to invite an external user?",
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
                    "text": "I have a different problem, not an invitation problem.",
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
            "id": "whoInvitee",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the email address of the person you’re trying to invite?",
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
            "id": "whichApp",
            "visibility": null,
            "order": 4,
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
