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
  "fileAttachmentHint": "Provide written (email) permission from the current  Account Administrator as an attachment to the case",
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
      "displayLabel": "Subscription ID that needs to be moved",
      "watermarkText": "Provide the Subscription ID that needs to be moved",
      "required": true
    },
    {
      "id": "accountadmin_details1",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Are you the current Account Administrator for this subscription?",
      "watermarkText": "Are you the current Account Administrator for this subscription?",
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
      "id": "accountadmin_details2",
      "order": 4,
      "visibility": "accountadmin_details1 == No",
      "controlType": "textbox",
      "displayLabel": " Email address of the current account admin for this subscription",
      "watermarkText": " Email address of the current account admin for this subscription",
      "required": true
    },
    {
      "id": "destinationemail_details",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": " Email address of new Account Administrator",
      "watermarkText": "Provide the destination email address of the Account Administrator for the account you want to transfer it to",
      "infoBalloonText": "This is the person to whom you want to transfer the subscription to",
      "required": true
    },
    {
      "id": "selfserve_details1",
      "order": 6,
      "visibility": "accountadmin_details1 == Yes",
      "controlType": "dropdown",
      "displayLabel": "Have you already tried <a href='https://docs.microsoft.com/azure/billing/billing-subscription-transfer'> self-serve subscription ownership transfer</a> option? ",
      "watermarkText": "Have you already tried self-serve subscription ownership transfer option? ",
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
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Details of error for the failure",
      "required": true,
      "watermarkText": "Provide details on the error for the failure "
    },
    {
      "id": "error_details2",
      "visibility": "accountadmin_details1 == Yes && selfserve_details1 == No",
      "order": 8,
      "controlType": "dropdown",
      "displayLabel": "Please try to <a href='https://docs.microsoft.com/azure/billing/billing-subscription-transfer'>transfer the subscription yourself using the self-serve option</a>. Did it solve your issue?",
      "required": false,
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        }
      ]
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
      "id": "problem_description_1",
      "visibility": "accountadmin_details1 == No && emailproof_details1 == Yes",
      "order": 10,
      "controlType": "multilinetextbox",
       "displayLabel": "Provide permission and any other details",
      "watermarkText": "Provide any additional details about the issue",
      "required": true,
      "hints": [
        {
          "text": "Provide written (email) permission from the current Account Administrator as an attachment to the case in the file upload below"
        }
      ]
    },
    {
      "id": "problem_description_2",
      "visibility": "accountadmin_details1 == No && emailproof_details1 == No",
      "order": 11,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide all relevant details",
      "watermarkText": "Provide all relevant details",
      "required": false,
      "hints": [
        {
          "text": "Please provide all relevant details of this request including why the current Account Administrator cannot provide permission and/or cannot perform themselves"
        }
      ]
    },
    {
      "id": "problem_description",
      "order": 12,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Additional Details (if any)",
      "watermarkText": "Provide any additional details about the issue",
      "required": true
    }
  ]
}
---
