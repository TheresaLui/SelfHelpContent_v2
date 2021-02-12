<properties
	pageTitle="Scoping questions for Change ownership of my subscription"
	description="Scoping questions for Subscription Management/Change ownership of my subscription"
	authors="prdasneo"
	ms.author="prdasneo"
          selfHelpType="problemScopingQuestions"
	supportTopicIds="32454918"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
    schemaVersion="1"
   articleId="3c613a21-eb24-4e91-bf21-d530a8f88c2e"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Change ownership of my subscription
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Change ownership of my subscription",
    "fileAttachmentHint": "If you are **not** the Account Admin, provide written (email) permission from the current  Account Admin as an attachment to the case",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "SubscriptionId",
            "order": 13,
            "controlType": "dropdown",
            "displayLabel": "Select the Subscription ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions?api-version=2014-04-01",
                "jTokenPath": "value",
                "textProperty": "displayName,subscriptionId",
                "textTemplate": "{displayName} ({subscriptionId})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "dont_know_answer",
                    "text": "Not in the list"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "subscriptionid_details",
            "order": 14,
            "visibility": "SubscriptionId == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": false
        },
        {
            "id": "accountadmin_details1",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you the current Account Admin for this subscription?",
            "watermarkText": "Are you the current Account Admin for this subscription?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "accountadmin_details2",
            "order": 4,
            "visibility": "accountadmin_details1 == No",
            "controlType": "textbox",
            "displayLabel": " Email address of the current Account Admin for this subscription",
            "watermarkText": " Email address of the current Account Admin for this subscription",
            "required": false
        },
        {
            "id": "destinationemail_details",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": " Email address of new Account Admin",
            "watermarkText": "Provide the destination email address of the Account Admin for the account you want to transfer it to",
            "infoBalloonText": "This is the person to whom you want to transfer the subscription to",
            "required": false
        },
        {
            "id": "selfserve_details1",
            "order": 6,
            "visibility": "accountadmin_details1 == Yes",
            "controlType": "dropdown",
            "displayLabel": "Did the self-serve subscription ownership transfer option solve your issue? Click the help bubble to learn more on this",
            "watermarkText": "Did the self-serve subscription ownership transfer option solve your issue? ",
            "infoBalloonText": " <a href='https://docs.microsoft.com/azure/billing/billing-subscription-transfer'>Transfer the subscription yourself using the self-serve option</a>.",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "error_details1",
            "visibility": "accountadmin_details1 == Yes && selfserve_details1 == No",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Details of error for the failure",
            "required": false,
            "watermarkText": "Provide details on the error for the failure "
        },
        {
            "id": "emailproof_details1",
            "order": 9,
            "visibility": "accountadmin_details1 == No",
            "controlType": "dropdown",
            "displayLabel": "Can you provide written (email) permission from the current  Account Admin for MSFT to perform the transfer on their behalf?",
            "watermarkText": "Can you provide written (email) permission from the current  Account Admin for MSFT to perform the transfer on their behalf?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description_1",
            "visibility": "accountadmin_details1 == No && emailproof_details1 == Yes",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide permission and any other details",
            "watermarkText": "Provide any additional details about the issue",
            "required": false
        },
        {
            "id": "problem_description_2",
            "visibility": "accountadmin_details1 == No && emailproof_details1 == No",
            "order": 11,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide all relevant details",
            "watermarkText": "Please provide all relevant details of this request including why the current Account Admin cannot provide permission and/or cannot perform themselves",
            "required": false,
            "infoBalloonText": "Please provide all relevant details of this request including why the current Account Admin cannot provide permission and/or cannot perform themselves"
        },
        {
            "id": "problem_description",
            "order": 12,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional Details (if any)",
            "watermarkText": "Provide any additional details about the issue",
            "required": true,
            "hints": [
                {
                    "text": "Note: Provide written (email) permission from the current Account Administrator as an attachment to the case in the file upload below"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
