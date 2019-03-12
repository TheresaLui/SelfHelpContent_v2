<properties
    pageTitle="Billing and Payment Issues"
    description="Billing and Payment Issues"
    ms.author="prdasneo"
    authors="prdasneo"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32454856,32632936"
    productPesIds="15659"
    articleId="b4b6273d-558e-4f2d-ab00-36a830ea4354"
    cloudEnvironments="public"
    schemaVersion="1"
/>

# Billing and Payment Issues
---
{
  "resourceRequired": false,
  "title": "Issues with Billing and Payment",
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
      "displayLabel": "Subscription ID",
      "watermarkText": "Provide your Subscription ID",
      "required": true
    },
    {
      "id": "payment_method",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Choose the type of Payment Method",
      "watermarkText": "Choose the type of Payment Method",
      "dropdownOptions": [
        {
          "value": "Invoice",
          "text": "Invoice"
        },
        {
          "value": "Credit Card",
          "text": "Credit Card"
        }
      ],
      "required": true
    },
    {
      "id": "invoiceid_details",
      "order": 4,
      "controlType": "textbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Invoice ID related to the issue",
      "watermarkText": "Provide your Invoice ID related to the issue",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Notifications received (if applicable)",
      "watermarkText": "Provide any notifications received regarding billing and payment issues",
      "required": true
    }
  ]
}
---
