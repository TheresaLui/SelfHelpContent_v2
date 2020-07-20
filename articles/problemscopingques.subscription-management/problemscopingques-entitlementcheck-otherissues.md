<properties
	pageTitle="Scoping questions for Entitlement Check and Other Issues"
	description="Scoping questions for Entitlement Check and Other Issues"
	authors="prdasneo"
	ms.author="prdasneo"
          selfHelpType="problemScopingQuestions"
	supportTopicIds="32632951,32632957"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
   articleId="EntitlementCheckandOtherIssue-problemscopingquestion"
	ownershipId="ASMS_SubscriptionManagement"
/>
#  Entitlement Check and Other Issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Entitlement Check and Other Issues",
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
            "id": "subscriptionid_details",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "Provide your Subscription id",
            "required": false
        },
        {
            "id": "offertype_details",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the Offer type",
            "watermarkText": "Select the type of offer",
            "dropdownOptions": [
                {
                    "value": "Action Pack",
                    "text": "Action Pack"
                },
                {
                    "value": "Enterprise Agreement",
                    "text": "Enterprise Agreement"
                },
                {
                    "value": "Enterprise Dev/Test",
                    "text": "Enterprise Dev/Test"
                },
                {
                    "value": "Microsoft Azure Sponsored Offer",
                    "text": "Microsoft Azure Sponsored Offer"
                },
                {
                    "value": "MSDN Platforms subscribers",
                    "text": "MSDN Platforms subscribers"
                },
                {
                    "value": "Pay-As-You-Go",
                    "text": "Pay-As-You-Go"
                },
                {
                    "value": "Pay-As-You-Go Dev/Test",
                    "text": "Pay-As-You-Go Dev/Test"
                },
                {
                    "value": "Visual Studio Enterprise",
                    "text": "Visual Studio Enterprise"
                },
                {
                    "value": "Visual Studio Enterprise (BizSpark)",
                    "text": "Visual Studio Enterprise (BizSpark)"
                },
                {
                    "value": "Visual Studio Enterprise (MPN)",
                    "text": "Visual Studio Enterprise (MPN)"
                },
                {
                    "value": "Visual Studio Professional",
                    "text": "Visual Studio Professional"
                },
                {
                    "value": "Visual Studio Test Professional",
                    "text": "Visual Studio Test Professional"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "offertype_details2",
            "order": 4,
            "visibility": "offertype_details == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": " Provide the Offer Type",
            "watermarkText": "Provide the Offer Type",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide a brief description of the issue",
            "watermarkText": "Provide a brief description of the issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
