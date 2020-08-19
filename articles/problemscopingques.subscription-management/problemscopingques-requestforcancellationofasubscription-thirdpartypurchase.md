<properties
	pageTitle="Request to re-enable a Subscription"
	description="Request to re-enable a Subscription"
	articleId="requestforcancellationofasubscriptionthirdpartypurchase"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632954"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Re-enable a Subscription
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Re-enable a Subscription",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
	{
            "id": "subscriptionid",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "",
            "required": true
        },
        {
            "id": "reason_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Reason for re-enabling",
            "watermarkText": "Provide the reason for re-enabling",
            "required": false
        },
        {
            "id": "error_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message encountered (if any)",
            "watermarkText": "Provide the error message encountered",
            "required": false
        },
	{
            "id": "email_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Email notification (if any) about subscription suspension",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details (if any)",
            "watermarkText": "Provide any other additional relevant details",
            "required": true
           }
    ],
    "$schema": "SelfHelpContent"
}
---
