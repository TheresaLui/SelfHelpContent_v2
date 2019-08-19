<properties pageTitle="Problem with inviting an external user" 
	 description="aadb2bissue" 
	 authors="marialai" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32615387" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
	articleId="problemscopingques-inviteb2buser"
/>
# Problem with inviting an external user
---
{
    "resourceRequired": false,
    "title": "Problem with inviting an external user",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whoInviter",
            "visibility": null,
            "order": 1,
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
                    "text": "Another user",
                    "value": "anotherUser"
                },
                {
                    "text": "I have a different problem, not an invitation problem.",
                    "value": "anotherProblem"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whoInvitee",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the email address of the person you’re trying to invite?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whichApp",
            "visibility": null,
            "order": 3,
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
                },
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whereProblem",
            "visibility": null,
            "order": 4,
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
                    "text": "B2B API",
                    "value": "invitationAPI"
                },
                {
                    "text": "Access panel",
                    "value": "accessPanel"
                },
                {
                    "text": "Other Application",
                    "value": "otherApp"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "other"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "errorText",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Paste in the error text, including the correlation ID if any.",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "URL",
            "visibility": null,
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "What is the URL of the page you saw the problem on?",
            "content": null,
            "watermarkText": "Enter the URL you were trying to access when the error happened. Note that the error page itself may have a URL, that’s not the one we need.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "reproStepsText",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What specific steps did you or the user follow that resulted in the error?",
            "content": null,
            "watermarkText": "List each specific step taken, and where those steps were performed.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 10
        },
    ],
    "$schema": "SelfHelpContent"
}
---
