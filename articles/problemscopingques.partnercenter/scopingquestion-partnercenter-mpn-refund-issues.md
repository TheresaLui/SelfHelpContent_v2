<properties
	pageTitle="Partner Center MPN refund issues"
	description="Partner Center MPN refund issues"
	authors="dimanjar" 
	ms.author="dimanjar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725802"
	productPesIds="17000"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_mpn_refund_issues"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Partner Center MPN refund issues
---
{
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "MPN refund issue",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "mpn_refund_issue_type",
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
          "value": "Cancellation of membership",
          "text": "Cancellation of membership"
        },
        {
          "value": "dont_know_answer",
          "text": "Other"
        }
      ],
      "required": true
    },
    {
      "id": "mpn_refund_reason",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please enter the reason for refund request",
      "watermarkText": "Refund reason",
      "required": false
    },
    {
      "id": "mpn_order_id",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Please enter the order ID you are having issue with",
      "watermarkText": "Order ID",
      "required": false
    },
   {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controltype": "datetimepicker",
            "displayLabel": "When did this issue start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
