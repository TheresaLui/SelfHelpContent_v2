<properties
	pageTitle="Questions on Spending Limits"
	description="Questions on Spending Limits"
	articleId="assistancewithbillandusage-questionsonspendinglimits-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632938"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	schemaVersion="1"
/>
#  Questions on Spending Limits
---
{
  "resourceRequired": false,
  "title": "Questions on Spending Limits",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "visibility": null,
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Problem Start Date",
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
            "required": true
        },
    {
      "id": "problem_description",
      "order": 3,
      "controlType": "multilinetextbox",
      "displayLabel": "Error message (if any)",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Describe your problem, providing as much detail as possible."
        }
      ]
    }
  ]
}
---
