<properties 
    pageTitle="Administrator-initiated password reset" 
	description="Password Management/Administrator-initiated password reset" 
	authors="sahenry" 
    ms.author="sahenry"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32045781" 
	productPesIds="16579" 
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	schemaVersion="1"
    articleId="c7a169ee-063e-4acd-a61e-44f17d01a0e6"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/> 
# Problem with administrator-initiated password reset 
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with password management",
    "fileAttachmentHint": null,
    "diagnosticCard": {
        "title": "Problem with password management administrator-initiated",
        "description": "Our self-service password reset troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your inputs."
    },
    "formElements": [
        {
            "id": "problem_description",
            "visibility": null,
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the username of the admin who is resetting the user's password?",
            "content": null,
            "watermarkText": "For example 'sarah@contoso.com'",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        },
        {
            "id": "userId",
            "visibility": null,
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which user is experiencing this problem?",
            "content": null,
            "watermarkText": "For example 'joe@contoso.com'.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0,
	    "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "timestamp",
            "visibility": null,
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Timestamp from Error message:",
            "content": null,
            "watermarkText": "Copy the timestamp from the error message and paste it here",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "symptomType",
            "visibility": null,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error that you are receiving?",
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
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
