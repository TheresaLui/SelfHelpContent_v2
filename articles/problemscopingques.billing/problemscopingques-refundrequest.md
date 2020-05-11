<properties
	pageTitle="Refund Request"
	description="Refund Request"
	articleId="refundrequest"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454868"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>

# Refund Request
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Refund Request",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem Start Date",
            "required": true
        },
        {
            "id": "refundamount_details",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Refund Amount",
            "watermarkText": "Provide the refund amount",
            "required": true
        },
        {
            "id": "refundreason_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Reason for the Refund ",
            "watermarkText": "Provide the reason for the refund",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Please provide any additional details (if any)",
	     "hints": [
                {
                    "text": "If you are an indirect EA customer, please log your request via <a href='ea.azure.com'>EA portal</a> only"
                }
	],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
