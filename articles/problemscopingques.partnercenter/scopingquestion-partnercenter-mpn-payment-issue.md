<properties
	pageTitle="Partner Center MPN payment issues"
	description="Partner Center MPN payment issues"
	authors="dimanjar" 
	ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635688"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_MPN_payment_issues"
	clientIds="partnercenter"
/>
#Partner Center MPN payment issues
---
{
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "MPN payment issue",
  "fileAttachmentHint": "Please attach the proof of payment",
  "formElements": [
    {
      "id": "mpn_payment_type",
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What is the mode of payment?",
      "watermarkText": "Select payment type",
      "dropdownOptions": [
        {
          "value": "Wire transfer",
          "text": "Wire transfer"
        },
        {
          "value": "Credit card",
          "text": "Credit card"
        },
      ],
      "required": true
    },
    {
      "id": "mpn_order_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please enter the order ID you are having issue with?",
      "watermarkText": "Order ID",
      "required": false
    },
	{
      "id": "mpn_wire_transfer_date",
      "order": 3,
	  "visibility": "mpn_payment_type == Wire transfer",   
      "controltype": "datetimepicker",
      "displayLabel": "When was wire transfer done?",
      "required": true
	}
	{
      "id": "mpn_wire_transfer_account",
      "order": 4,
	  "visibility": "mpn_payment_type == Wire transfer",   
      "controltype": "textbox",
      "displayLabel": "Please enter the microsoft account to which wire transfer was done",
      "required": true
	}
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Details",
      "watermarkText": "Please provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "problem_start_time",
      "order": 6,
      "controltype": "datetimepicker",
      "displayLabel": "When did this issue start?",
      "required": true
    }
  ]
}
---
