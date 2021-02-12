<properties
	pageTitle="Partner Center MPN taxes issues"
	description="Partner Center MPN taxes issues"
	authors="dimanjar" 
	ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725825"
	productPesIds="17007"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_mpn_taxes_issues"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Partner Center MPN taxes issues
---
{
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "MPN taxes issue",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "mpn_invoice_taxes_type",
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Please select issue type?",
      "watermarkText": "Issue type",
      "dropdownOptions": [
        {
          "value": "Tax refund",
          "text": "Tax refund"
        },
        {
          "value": "Incorrect tax calculation",
          "text": "Incorrect tax calculation"
        },
        {
          "value": "dont_know_answer",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "mpn_order_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please enter the order ID you are having issue with",
      "watermarkText": "Order ID",
      "required": false
    },
   {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
