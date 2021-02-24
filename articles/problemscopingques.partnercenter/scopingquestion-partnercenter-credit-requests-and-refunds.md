<properties
	pageTitle="Partner Center Billing and Invoicing Credit Requests and refunds"
	description="Partner Center Credit Requests and refunds"
	authors="FeliceFan"
	ms.author="v-felice"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32692597"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_credit_requests_and_refunds"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center Credit Requests and Refunds
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Credit Requests and Refunds",
    "fileAttachmentHint": "Ensure to attach the credit request and refund form before submitting the service request.",
    "formElements": [
        {
            "id": "pc_subscription_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the subscription id you are request credit for.",
            "watermarkText": "Provide the subscription as a GUID",
            "required": false
        },
        {
            "id": "pc_order_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the order id you are request credit for.",
            "watermarkText": "Provide the order id",
            "required": false
        },
        {
            "id": "pc_customertenant_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant id you are purchasing for.",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
	    {
            "id": "# of customers impacted",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "# of customers impacted",
            "watermarkText": "Provide the number of customers impacted.",
            "required": false
        },
        {
            "id": "billing_admin_email_address",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please include the Billing admin email address for your organization to have visibility of credits on monthly invoice/reconciliation file.",
            "watermarkText": "To include multiple contacts, use a comma to separate each contact",
            "required": true,
            "useAsAdditionalDetails": true
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
