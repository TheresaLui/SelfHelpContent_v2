<properties
	pageTitle="CSP analyze and reporting"
	description="CSP analyze and reporting"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635633"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques_partnercenter_reporting"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# CSP analyze and reporting
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Questions about CSP analyze and reporting",
    "fileAttachmentHint": "Attach a file or screenshot that shows your question or issue.",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about the problem.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        },
	{
            "id": "csp_reporting",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What kind of reporting issue are you seeing?",
            "watermarkText": "What kind of reporting issue are you seeing?",
            "dropdownOptions": [
                {
                    "value": "Billing reporting",
                    "text": "Billing reporting"
                },
                {
                    "value": "Connecting to Power BI",
                    "text": "Connecting to Power BI"
                },
                {
                    "value": "Cost breakdown",
                    "text": "Cost breakdown"
                },
                {
                    "value": "Usage reporting",
                    "text": "Usage reporting"
                },
                {
                    "value": "Azure spending",
                    "text": "Azure spending"
                },
                {
                    "value": "Some other issue",
                    "text": "Some other issue"
                }
                ],
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
