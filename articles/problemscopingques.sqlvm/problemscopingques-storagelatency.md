<properties pageTitle="Storage Latency"
	 description="Storage Latency"
	 authors="yareyes"
     ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32633524"
	 productPesIds="14745"
	 cloudEnvironments="public"
	 schemaVersion="1"
	 articleId="0b40b41d-43b2-4f26-8f8a-2c325cbe004b"
/>
# Storage Latency
---
{
    "resourceRequired": false,
    "title": "Storage Latency",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "whichStorage",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What storage tier is being used for your databases?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Standard Storage",
                    "value": "StandardStorage"
                },
                {
                    "text": "Premium Storage",
                    "value": "PremiumStorage"
                },
                {
                    "text": "Ultra SSD",
                    "value": "UltraSSD"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "NotSure"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
