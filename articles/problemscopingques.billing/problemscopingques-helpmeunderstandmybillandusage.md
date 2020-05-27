<properties
	pageTitle="Help Me Understand My Bill and Usage"
	description="Help Me Understand My Bill and Usage"
	articleId="assistancewithbillandusage-helpmeunderstandmybillandusage-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632935"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>

#  Help Me Understand My Bill and Usage
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Help Me Understand My Bill and Usage",
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
            "id": "invoiceid_details",
            "order": 2,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Invoice # (if applicable)",
            "watermarkText": "Provide your Invoice#. If you dont have any, please use N/A",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide details about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Describe your problem, providing as much detail as possible."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
