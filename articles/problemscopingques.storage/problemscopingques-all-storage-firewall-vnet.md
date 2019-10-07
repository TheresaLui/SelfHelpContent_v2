<properties
	pageTitle="Storage Firewall and VNet"
	description="Storage Firewall and VNet scoping question"
	authors="AngshumanNayakMSFT"
	ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32682428,32682429,32682430,32682433,32682434,32682435,32682438,32682439,32682440,32682443,32682444,32682445"
	productPesIds="15629,16459,16462,16461,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="StorageScoping_all_firewall_Vnet"
/>
# Storage Firewall and VNet
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Firewall and VNet scoping question",
    "fileAttachmentHint": "",
    "formElements": [
         { "id": "problem_start_time",
          "order": 1,
          "controlType": "datetimepicker",
          "displayLabel": "Local start time of the latest occurrence",
          "required": true
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
                    "value": "other",
                    "text": "Not listed above"
                }
            ],
            "required": false
        },
        {
            "id": "request_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Storage server Request ID",
            "watermarkText": "Request ID of failed operation ending with 000000",
            "textPropertyRegex": "^([0-9A-Za-z]{8}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{4}[-][0-9A-Za-z]{6}[0]{6})$",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
