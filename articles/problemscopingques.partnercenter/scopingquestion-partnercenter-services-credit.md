<properties
	pageTitle="Partner Center Services Credit"
	description="Partner Center Services Credit"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635664"
	productPesIds="15960"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="sproblemscopingques_services_credit"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Partner Center Services Credit
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Services Credit",
    "fileAttachmentHint": "Ensure to attach the credit request and refund form before submitting the service request.",
    "formElements": [
        {
            "id": "pc_subscription_id",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Please provide the subscription id you want credit for.",
            "watermarkText": "Provide the subscription as a GUID",
            "required": false
        },
        {
            "id": "pc_customertenant_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Please provide the customer tenant id you want credit for.",
            "watermarkText": "Provide the customer tenant id as a GUID",
            "required": false
        },
               {
            "id": "pc_incident_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide the outage incident ID",
            "watermarkText": "Please provide the outage incident ID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
