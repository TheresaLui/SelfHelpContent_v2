<properties
	pageTitle="Request for Cancellation of a Subscription"
	description="Request for Cancellation of a Subscription"
	articleId="requestforcancellationofasubscriptionazuresubscriptions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632949"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Azure Subscription Cancellation
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Request for Cancellation of a Subscription",
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
            "id": "subscriptionId",
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
            "displayLabel": "Reason for cancellation",
            "watermarkText": "Provide the reason for cancellation",
            "required": false
        },
        {
            "id": "error_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message (if any) encountered ",
            "watermarkText": "Provide the error message encountered",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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
