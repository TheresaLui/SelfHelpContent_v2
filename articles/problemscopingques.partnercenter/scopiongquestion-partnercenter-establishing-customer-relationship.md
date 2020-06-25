<properties
	pageTitle="Partner Center Establishing Customer Relationship"
	description="Partner Center Establishing Customer Relationship"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725888"
	productPesIds="17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_establishing_customer_relationship"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"
/>
# Partner Center Establishing Customer Relationship
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Establishing Customer Relationship",
    "fileAttachmentHint": "Please attach screenshots that show the problem you are having.",
    "formElements": [
        {
            "id": "crquestion_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is your question about?",
            "watermarkText": "What is your question about?",
            "dropdownOptions": [
                {
                    "value": "Customer error accepting your relationship",
                    "text": "Customer error accepting your relationship"
                },
                {
                    "value": "Problems supporting the customer after they accept",
                    "text": "Problems supporting the customer after they accept"
                },
                {
                    "value": "Problems purchasing products for the customer after they accept",
                    "text": "Problems purchasing products for the customer after they accept"
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
