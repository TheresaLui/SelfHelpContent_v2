<properties
	pageTitle="Switch to Another Offer"
	description="Switch to Another Offer"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454938,32632959"
	productPesIds="15660"
	cloudEnvironments="public, Mooncake"
	schemaVersion="1"
	articleId="switchtoanotheroffer"
/>


# Switch to Another Offer
---
{
  "resourceRequired": false,
  "title": "Switch to Another Offer",
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
      "id": "problem_description",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide a brief description of the issue",
      "watermarkText": "Provide a brief description of the issue",
      "useAsAdditionalDetails": true,
      "required": true,
      "hints": [
        {
          "text": "Note: The solution provided is limited to <a href='https://docs.microsoft.com/azure/billing/billing-how-to-switch-azure-offer'> Pay As You Go </a> only. To Convert to any other offer, please provide the below details:"
        }
      ]
    },
    {
      "id": "subscriptionid_details",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Subscription ID",
      "watermarkText": "Provide the Subscription ID",
      "required": true
    },
    {
      "id": "offertype_details",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Select the new Offer type to convert to",
      "watermarkText": "Select the new Offer type to convert to",
      "dropdownOptions": [
        {
          "value": "Action Pack",
          "text": "Action Pack"
        },
        {
          "value": "Enterprise Agreement",
          "text": "Enterprise Agreement"
        },
        {
          "value": "Enterprise Dev/Test",
          "text": "Enterprise Dev/Test"
        },
        {
          "value": "Microsoft Azure Sponsored Offer",
          "text": "Microsoft Azure Sponsored Offer"
        },
        {
          "value": "MSDN Platforms subscribers",
          "text": "MSDN Platforms subscribers"
        },
        {
          "value": "Pay-As-You-Go",
          "text": "Pay-As-You-Go"
        },
        {
          "value": "Pay-As-You-Go Dev/Test",
          "text": "Pay-As-You-Go Dev/Test"
        },
        {
          "value": "Visual Studio Enterprise",
          "text": "Visual Studio Enterprise"
        },
        {
          "value": "Visual Studio Enterprise (BizSpark)",
          "text": "Visual Studio Enterprise (BizSpark)"
        },
        {
          "value": "Visual Studio Enterprise (MPN)",
          "text": "Visual Studio Enterprise (MPN)"
        },
        {
          "value": "Visual Studio Professional",
          "text": "Visual Studio Professional"
        },
        {
          "value": "Visual Studio Test Professional",
          "text": "Visual Studio Test Professional"
        },
        {
          "value": "dont_know_answer",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "offertype_details2",
      "order": 5,
      "visibility": "offertype_details == Other",
      "controlType": "textbox",
      "displayLabel": " Provide the Offer Type",
      "watermarkText": "Provide the Offer Type",
      "required": true
    }
  ]
}
---
