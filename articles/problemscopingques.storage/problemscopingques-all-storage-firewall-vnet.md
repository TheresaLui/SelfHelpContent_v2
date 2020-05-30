<properties
	pageTitle="Storage Firewall and VNet"
	description="Storage Firewall and VNet scoping question"
	authors="AngshumanNayakMSFT"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32682428,32682429,32682430,32682433,32682434,32682435,32682438,32682439,32682440,32682443,32682444,32682445"
	productPesIds="15629,16459,16462,16461,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="StorageScoping_all_firewall_Vnet"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Storage Firewall and VNet

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Firewall and VNet scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Firewall & VNet Issues Troubleshooter",
        "description": "If you are reporting about an issue please help us with a few inputs and give us couple of minutes to run automated diagnostics. We can help diagnose your problem without the need of opening a support ticket.",
        "insightNotAvailableText": "Our automated troubleshooter did not detect any issues with your resource. You can help us by providing the right inputs below and ensuring that the format is as suggested in the watermark."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Local start time of the latest occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "error_code_dropdown",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Error code",
            "watermarkText": "HTTP error of failed operation",
            "dropdownOptions": [
                {
                    "value": "HTTP_400",
                    "text": "HTTP 400"
                },
                {
                    "value": "HTTP_403",
                    "text": "HTTP 403"
                },
                {
                    "value": "HTTP_404",
                    "text": "HTTP 404"
                },
                {
                    "value": "HTTP_409",
                    "text": "HTTP 409"
                },
                {
                    "value": "HTTP_500",
                    "text": "HTTP 500"
                },
                {
                    "value": "HTTP_501",
                    "text": "HTTP 501"
                },
                {
                    "value": "HTTP_502",
                    "text": "HTTP 502"
                },
                {
                    "value": "HTTP_503",
                    "text": "HTTP 503"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not listed above"
                }
            ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "request_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Storage server Request ID",
            "watermarkText": "Request ID of failed operation ending with 000000",
            "textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "You can follow our guideline to <a href='https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting'>monitor, diagnose, and troubleshoot Microsoft Azure Storage</a> issues."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
