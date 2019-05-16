<properties
	pageTitle="Billing API"
	description="Billing API"
	articleId="billingapi"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599495"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Billing API
---
{
  "resourceRequired": false,
  "title": "Billing API",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "visibility": null,
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Problem start time",
      "required": true
    },
   {
            "id": "SubscriptionId",
            "order": 6,
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
            "order": 7,
            "visibility": "SubscriptionId == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": false
        },
{
      "id": "emailid_details",
      "order": 3,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Email ID accessing the data",
      "watermarkText": "Provide the email id accessing the data",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional details",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Error Message"
        }
      ]
    }
  ]
}
---
