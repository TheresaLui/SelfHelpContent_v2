<properties
	pageTitle="Partner Center Invoice and Billing Issue"
	description="Partner Center Invoice and Billing Issue"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32692599,32692601,32725827,32692608"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_invoices"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center Invoice and Billing Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Invoice and Billing Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_invoice_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What kind of invoice is your issue about?",
            "watermarkText": "Select invoice type",
            "dropdownOptions": [
                {
                    "value": "Recurring",
                    "text": "Recurring"
                },
                {
                    "value": "One-time",
                    "text": "One-time"
                }
            ],
            "required": false
        },
	        {
            "id": "pc_invoice_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the invoice id you have issues with.",
            "watermarkText": "Provide the invoice id",
            "required": false
        },
        {
            "id": "pc_subscription_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the subscription id you have issues with.",
            "watermarkText": "Provide the subscription id (GUID)",
            "required": false
        },
        {
            "id": "pc_recon_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What kind of recon file is your issue about?",
            "watermarkText": "Select recon file type",
            "dropdownOptions": [
                {
                    "value": "Recurring license-based",
                    "text": "Recurring license-based"
                },
                {
                    "value": "Recurring usage-based",
                    "text": "Recurring usage-based"
                },
                {
                    "value": "One-time purchases",
                    "text": "One-time purchases"
                }
            ],
            "required": false
        },
	{
            "id": "#_of_customers_impacted",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "# of customers impacted",
            "watermarkText": "Please provide the number of customers impacted.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
