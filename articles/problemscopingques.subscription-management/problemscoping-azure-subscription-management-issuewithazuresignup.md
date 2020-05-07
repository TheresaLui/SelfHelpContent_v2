<properties
	pageTitle="Scoping questions for Issue with Azure sign-up"
	description="Scoping questions for Subscription Management/Issue with Azure sign-up"
	authors="prdasneo"
	ms.author="prdasneo"
   selfHelpType="problemScopingQuestions"
   supportTopicIds="32632950"
	productPesIds="15660"
	cloudEnvironments="public, MoonCake, Fairfax, Blackforest, usnat, ussec"
   schemaVersion="1"
   articleId="problemscopingquestion-azure-sign-up"
	ownershipId="ASMS_SubscriptionManagement"
/>
# Issue with Azure purchase
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Signup Issues - Azure Subscriptions",
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
            "id": "phonenumber_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Phone number used during sign-up",
            "watermarkText": "Provide the Phone number used during sign-up",
            "required": false
        },
	{
            "id": "emailid_details",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Email address used during sign-up",
            "watermarkText": "Provide the Email address used during sign-up",
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
