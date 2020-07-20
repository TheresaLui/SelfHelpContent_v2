<properties
	pageTitle="Partner Center Users Notifications"
	description="Partner Center Users Notifications"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32728287,32728293,32725812"
	productPesIds="17000"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_users_notifications"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Partner Center Users Notifications
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Users Notifications",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pc_userproblem_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What user accounts are you having problems with?",
            "watermarkText": "User: username@onmicrosoft.com",
            "required": false
        },
        {
            "id": "notification_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of notifications are you having problems with?",
            "watermarkText": "What type of notifications are you having problems with?",
            "dropdownOptions": [
                {
                    "value": "Invoice is available",
                    "text": "Invoice is available"
                },
                {
                    "value": "Azure spending thresholds",
                    "text": "Azure spending thresholds"
                },
                {
                    "value": "Customer Service health",
                    "text": "Customer Service health"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
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
