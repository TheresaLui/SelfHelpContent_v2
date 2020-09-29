<properties
	pageTitle="Scoping questions for Issue with Azure purchase"
	description="Scoping questions for Subscription Management/Issue with Azure purchase"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632948"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake, Blackforest, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="8297852a-5e4f-41d8-ae24-9e37aaa5714a"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Issue with Azure purchase
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Purchase Issues - Azure Subscriptions",
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
            "id": "phonenumber_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Phone number used during purchase",
            "watermarkText": "Provide the Phone number used during purchase",
            "required": false
        },
	{
            "id": "emailid_details",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Email address used during purchase",
            "watermarkText": "Provide the Email address used during purchase",
            "required": false
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
