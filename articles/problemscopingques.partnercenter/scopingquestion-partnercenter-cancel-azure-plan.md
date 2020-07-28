<properties
	pageTitle="Partner Center Cancel Azure plan without RBAC"
	description="Partner Center Cancel Azure plan without RBAC"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725882"
	productPesIds="17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_cancel_azure_plan"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"
/>
# Partner Center Cancel Azure plan without RBAC
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Cancel Azure plan without RBAC",
    "fileAttachmentHint": "Please attach a screenshot or any other files that may help explain your request.",
    "formElements": [
	{
            "id": "pc_customer_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the first and last name of your customer",
            "watermarkText": "First and last name",
            "required": false
        },
	{
            "id": "pc_customer_phone",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide a contact name for the customer",
            "required": false
        },
	{
            "id": "pc_customer_email",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the contact email address for your customer",
            "required": true
        },
	{
            "id": "pc_customertenant_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Please provide the tenant id for the customer that has the Azure plan you would like to cancel",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please the reason you need to cancel this Azure plan for this customer",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
