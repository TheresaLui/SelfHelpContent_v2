<properties
	pageTitle="Scoping questions for Issue with Azure Subscription conversion"
	description="Scoping questions for Subscription Management/Issue with Azure Subscription conversion"
	authors="prdasneo"
	ms.author="prdasneo"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32632955,32680690"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake, Fairfax, Blackforest, usnat, ussec"
   schemaVersion="1"
   articleId="problemscopingquestion-issuewith-azure-subscription-conversion"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Issue with Azure Subscription conversion
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Subscription conversion Issues - Azure Subscriptions",
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
            "id": "subscription_details",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "",
            "required": true
        },
        {
            "id": "error_details",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message (if any)",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Issue description",
            "watermarkText": "Provide any additional information about your issue",
            "required": true
	    }
    ],
    "$schema": "SelfHelpContent"
}
---
