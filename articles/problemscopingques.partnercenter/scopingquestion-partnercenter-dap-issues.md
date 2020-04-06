<properties
	pageTitle="Partner Center DAP Issues"
	description="Partner Center DAP Issues"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635675"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="sproblemscopingques_dap_issues"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
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
            "displayLabel": "Please provide the customer tenant id you are having problems with",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---