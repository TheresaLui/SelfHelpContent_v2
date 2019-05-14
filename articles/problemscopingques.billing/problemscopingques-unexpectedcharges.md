<properties
	pageTitle="Unexpected Charges"
	description="Unexpected Charges"
	articleId="unexpectedcharges-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632931"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	schemaVersion="1"
/>
# Unexpected Charges
---
{
  "resourceRequired": true,
  "title": "Unexpected Charges",
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
            "id": "SubscriptionId",
            "order": 7,
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
            "order": 8,
            "visibility": "SubscriptionId == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": true
        },
    {
      "id": "service_details",
      "order": 3,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Service causing the charges",
      "watermarkText": "Provide the Service causing the charges",
      "required": false
    },
    {
      "id": "impact_details",
      "order": 4,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Impacted duration",
      "watermarkText": "Provide the Impacted duration",
      "required": false
    },
    {
      "id": "invoiceid_details",
      "order": 5,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Invoice ID related to the issue",
      "watermarkText": "Provide the Invoice ID related to the issue",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Brief summary of the issue",
      "watermarkText": "Provide brief summary of the issue",
      "required": true
    }
  ]
}
---
