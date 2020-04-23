<properties
	pageTitle="Switch to Pay by Invoice"
	description="Switch to Pay by Invoice"
	articleId="payment-switchtopaybyinvoice-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632941"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Switch to Pay by Invoice
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Pay by Invoice",
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
            "id": "customer_details1",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "New or Existing customer?",
            "watermarkText": "",
            "dropdownOptions": [
                {
                    "value": "New Customer",
                    "text": "New Customer"
                },
                {
                    "value": "Existing Customer",
                    "text": "Existing Customer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "customer_details2",
            "order": 3,
            "visibility": "customer_details1 == Existing Customer",
            "controlType": "textbox",
            "displayLabel": "Current Payment Method",
            "watermarkText": "",
            "required": false
        },
	{
            "id": "customer_details3",
            "order": 15,
            "controlType": "dropdown",
            "displayLabel": "Do you have any outstanding balance?",
            "watermarkText": "",
	    "infoBalloonText": "Check <a href='https://docs.microsoft.com/azure/billing/billing-download-azure-invoice-daily-usage-date#download-usage'>this </a> to resolve any outstanding balance",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
	{
            "id": "orderid_details",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Order ID (requesting for invoice option)",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "accountadminid_details",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Account Admins Live ID(or Org ID) (should be company domain)",
            "watermarkText": "",
            "infoBalloonText": "Learn more: <a href='https://docs.microsoft.com/azure/billing/billing-add-change-azure-subscription-administrator'> Account Admin's email address</a>.",
            "required": true
        },
        {
            "id": "commerceaccountid_details",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Commerce Account ID",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "country_details",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Country",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "taxvatid_details",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "TAX ID/ VAT ID",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "microsoftassociation_details1",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Any prior business with Microsoft?",
            "watermarkText": "",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "contactname_details",
            "order": 10,
            "controlType": "textbox",
            "displayLabel": "Contact Name",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "contactphone_details",
            "order": 11,
            "controlType": "textbox",
            "displayLabel": "Contact Phone",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "contactemail_details",
            "order": 12,
            "controlType": "textbox",
            "displayLabel": "Contact Email",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 13,
            "controlType": "multilinetextbox",
            "displayLabel": "Company details",
            "watermarkText": "Provide the company details",
            "required": true,
            "hints": [
                {
                    "text": "Company Name (as registered under VAT or Government Website)"
                },
                {
                    "text": "Company Address (as registered under VAT or Government Website)"
                },
                {
                    "text": "Company Website"
                },
                {
                    "text": "Company Established on (Year) (for invoice onboarding only)"
                }
            ]
        },
        {
            "id": "justification_details",
            "order": 14,
            "controlType": "multilinetextbox",
	    "useAsAdditionalDetails": true,
            "displayLabel": "Provide justification on why you prefer Invoice option over credit card",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
