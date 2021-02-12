<properties
	pageTitle="Partner Center Billing and Payments - Payments"
	description="Partner Center Billing and Payments - Payments"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32692605"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques_billing_payments"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center Billing and Payments - Payments
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Billing and Payments",
    "fileAttachmentHint": "Please attach proof of payment in doc or pdf format if required.",
    "formElements": [
        {
            "id": "pc_payment_not_reflected",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this request about a payment sent but not reflected in Partner Center?",
            "watermarkText": "Is this request about a payment sent but not reflected in Partner Center?",
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
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
	{
            "id": "#_of_customers_impacted",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "# of customers impacted",
            "watermarkText": "Please provide the number of customers impacted.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please describe the question you have around payments. If you are not seeing payments reflected in Partner Center please be sure to attach a proof of payment.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
