<properties
	pageTitle="Partner Center DAP Issues"
	description="Partner Center DAP Issues"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32725889"
	productPesIds="17012"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_dap_issues"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Transact_and_Manage"
/>
# Partner Center DAP Issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center DAP Issues",
    "fileAttachmentHint": "Please attach a screenshot of the issue or error you are having",
    "formElements": [
        {
            "id": "pc_customertenant_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Affected Customer's domain or tenant ID",
            "watermarkText": "Please provide the affected customer's domain or tenant ID",
            "required": false
        },
	{
            "id": "azure_subscription_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Affected Azure Subscription ID",
            "watermarkText": "Please provide the affected azure subscription ID",
            "required": false
        },
	{
            "id": "user_account_information",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Affected User account information with error",
            "watermarkText": "Please provide the affected user account information with error",
            "required": false
        },
	{
            "id": "user_account_to_validate",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "User account for who it is working to validate",
            "watermarkText": "Please provide the user account for who it is working to validate",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
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
