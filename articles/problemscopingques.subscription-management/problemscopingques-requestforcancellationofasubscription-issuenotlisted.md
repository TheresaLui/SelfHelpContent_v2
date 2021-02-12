<properties
	pageTitle="Request for Cancellation of a Subscription - issue not listed"
	description="Request for Cancellation of a Subscription - issue not listed"
	articleId="requestforcancellationofasubscriptionissuenotlisted"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680688"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_SubscriptionManagement"
/>

#  Request for Cancellation of a Subscription- issue not listed
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Request for Cancellation of a Subscription - issue not listed",
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
            "id": "error_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message encountered (if any)",
            "watermarkText": "Provide the error message encountered",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details (if any)",
            "watermarkText": "Describe your problem, providing as much detail as possible",
            "required": true
	    }
    ],
    "$schema": "SelfHelpContent"
}
---
