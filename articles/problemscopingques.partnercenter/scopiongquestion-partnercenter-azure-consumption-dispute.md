<properties
	pageTitle="Partner Center Azure Consumption Dispute"
	description="Partner Center Azure Consumption Dispute"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32692593"
	productPesIds="17003"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_azure_consumption_dispute"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Billing_and_Invoicing"
/>
# Partner Center Azure Consumption Dispute
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Azure Consumption Dispute",
    "fileAttachmentHint": "Please attach reconciliation files and screenshots that show the problem you are having.",
    "formElements": [
        {
            "id": "crquestion_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is your question about?",
            "watermarkText": "What is your question about?",
            "dropdownOptions": [
                {
                    "value": "Problems establishing an Azure spending budget for your customer",
                    "text": "Problems establishing an Azure spending budget for your customer"
                },
                {
                    "value": "Questions or help with Non-payment, fraud, or misuse",
                    "text": "Questions or help with Non-payment, fraud, or misuse"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "pc_customer_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant ID (GUID) you are having problems with.",
            "watermarkText": "Customer tenant ID (GUID) you are having problems with",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please describe specifically what your question is about.",
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
