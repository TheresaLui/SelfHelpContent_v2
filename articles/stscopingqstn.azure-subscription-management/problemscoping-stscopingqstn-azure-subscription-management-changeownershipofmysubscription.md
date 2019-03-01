<properties
	pageTitle="Scoping questions for Change ownership of my subscription"
	description="Scoping questions for Subscription Management/Change ownership of my subscription"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454918"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake"
	schemaVersion="1"
	articleId="3c613a21-eb24-4e91-bf21-d530a8f88c2e"
/>
# Change ownership of my subscription
---
{
  "resourceRequired": false,
  "title": "Change ownership of my subscription",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Problem Start Date",
      "required": true
    },
    {
      "id": "subscriptionid_details",
      "order": 2,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Subscription ID that needs to be moved",
      "watermarkText": "Provide the Subscription ID that needs to be moved",
      "required": true
    },
    {
      "id": "accountadmin_details1",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Are you the current Account Administrator of the account where the subscription currently resides?",
      "watermarkText": "Are you the current Account Administrator of the account where the subscription currently resides?",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        }
      ],
      "required": true
    },
    {
      "id": "destinationemail_details",
      "order": 4,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Destination email address of the Account Administrator for the account you want to transfer it to",
      "watermarkText": "Provide the destination email address of the Account Administrator for the account you want to transfer it to",
      "required": true
    },
    {
      "id": "selfserve_details1",
      "order": 5,
      "visibility": "accountadmin_details1 == Yes",
      "controlType": "dropdown",
      "displayLabel": "Have you already tried self-serve Subscription Ownership Transfer option? ",
      "watermarkText": "Have you already tried self-serve Subscription Ownership Transfer option? ",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        }
      ],
      "required": true
    },
    {
      "id": "error_details1",
      "visibility": "accountadmin_details1 == Yes && selfserve_details1 == Yes",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Details of Error for the failure",
      "watermarkText": "Provide the details of error for the failure",
      "required": true
    },
    {
      "id": "error_details2",
      "visibility": "accountadmin_details1 == Yes && selfserve_details1 == No",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "Please try the self-serve SOT option",
      "watermarkText": "Please try the self-serve SOT option",
      "required": false
    },
    {
      "id": "accountadmin_details2",
      "order": 8,
      "visibility": "accountadmin_details1 == No",
      "controlType": "textbox",
      "displayLabel": "Current Account Administrator email address of the account where the subscription resides",
      "watermarkText": "Current Account Administrator email address of the account where the subscription resides",
      "required": true
    },
    {
      "id": "emailproof_details1",
      "order": 9,
      "visibility": "accountadmin_details1 == No",
      "controlType": "dropdown",
      "displayLabel": "Can you provide written (email) permission from the current  Account Administrator for MSFT to perform the transfer on their behalf?",
      "watermarkText": "Can you provide written (email) permission from the current  Account Administrator for MSFT to perform the transfer on their behalf?",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        }
      ],
      "required": true
    },
    {
      "id": "emailproof_details2",
      "visibility": "accountadmin_details1 == No && emailproof_details1 == Yes",
      "order": 10,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide written (email) permission from the current  Account Administrator as an attachment to the case",
      "watermarkText": "Provide written (email) permission from the current  Account Administrator as an attachment to the case",
      "required": false
    },
    {
      "id": "emailproof_details3",
      "visibility": "accountadmin_details1 == No && emailproof_details1 == No",
      "order": 11,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide all relevant details",
      "watermarkText": "Please provide all relevant details of this request including why the current  Account Administrator cannot provide permission and\/or cannot perform themselves",
      "required": false
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
          "text": "Learn more <a href='https://docs.microsoft.com/azure/billing/billing-subscription-transfer'> self-serve Subscription Ownership Transfer</a>."
        }
      ]
    }
  ]
}
---
