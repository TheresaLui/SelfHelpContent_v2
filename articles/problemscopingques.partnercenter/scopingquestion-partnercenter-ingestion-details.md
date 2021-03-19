<properties
	pageTitle="Partner Center Ingestion Details"
	description="Partner Center updated Ingestion Details"
	authors="A-COFLOR"
	ms.author="A-COFLOR"
	selfHelpType="problemScopingQuestions"
	supportTopicIds=""
	productPesIds="17006"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques_update_ingestion_details"
	clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Partner Center Ingestion Details
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Partner Center Ingestion Details",
    "fileAttachmentHint": "Please upload any supporting files that can help us understand your issue",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Please provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Start Time",
            "watermarkText": "When did your issue begin?",
            "required": true
        },
        {
            "id":"infoballoon_multidrop",
            "order":3,
            "infoBalloonText": "<a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>How to capture a browser trace for troubleshooting</a>",
            "controlType":"multiselectdropdown",
            "dropdownOptions": [
                {
                "value": "Option one",
                "text": "First option to select"
                },
                {
                "value": "Option two",
                "text": "Second option to select"
                },
                {
                "value": "Option three",
                "text": "Third option to select"
                },
                {
                "value": "Option four",
                "text": "Fourth option to select"
                },
		{
                "value": "Option five",
                "text": "Fifth option to select"
                },
		{
                "value": "Option six",
                "text": "Sixth option to select"
                },
		{
                "value": "Option seven",
                "text": "Seventh option to select"
                }
		],
            "displayLabel":"Please IGNORE this section as it is part of an operations test",
            "watermarkText":"Please IGNORE this section",
            "required": false
        },
        {
            "id": "infoballoon_singletest",
            "order": 4,
            "infoBalloonText": "<a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>How to capture a browser trace for troubleshooting</a>",
            "controlType": "textbox",
            "displayLabel": "Please IGNORE this section as it is part of an operations test",
            "watermarkText": "Please IGNORE this section",
            "required": false
        },
	{
            "id": "numeric_texttest",
            "order": 5,
            "controlType": "numerictextbox",
            "displayLabel": "Please IGNORE this section as it is part of an operations test - numeric",
            "watermarkText": "Please IGNORE this section",
            "required": false
        },
        {
            "id": "learn_more_text",
            "order": 6,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>Learn more</a> on how to capture a browser trace for troubleshooting"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
