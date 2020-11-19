<properties
    pageTitle="problem-with-self-service-sign-up-for-guest-users"
    description="Problem with self-service sign up for guest users" 
    authors="jkdouglas" 
    ms.author="jodougla"
    selfHelpType="problemScopingQuestions" 
    supportTopicIds="32741680" 
    productPesIds="16578" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    schemaVersion="1"
    articleId="problemscopingques-aadb2bselfservicesignupissue"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>
# Problem with self-service sign up for guest users
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with self-service sign up for guest users",
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
            "id": "problemUser",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Who is having an issue with self-service sign up?",
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
                    "text": "I have a different problem, not an self-service sign up problem.",
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
            "id": "signUpIssueType",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this an issue with configuring self-service sign up or an end user signing up?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Admin issue",
                    "value": "admin"
                },
                {
                    "text": "End user signing up",
                    "value": "endUser"
                },
		{
                    "text": "I am not sure what type of issue it is.",
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
            "order": 4,
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
            "order": 5,
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
            "order": 6,
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
            "order": 7,
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
