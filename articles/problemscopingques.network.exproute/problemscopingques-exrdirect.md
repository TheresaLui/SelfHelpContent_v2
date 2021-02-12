<properties
    pageTitle="Azure ExpressRoute Direct"
    description="Azure ExpressRoute Direct"
    authors="TobyTu"
    ms.author="Mario.Liu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32627976"
    productPesIds="15480"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b4b6173d-8533-4f2d-8526-36a830ea0098"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Azure ExpressRoute Direct questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure ExpressRoute Direct",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "loa_receive",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you received a Letter of Authorization (LOA) from Microsoft?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
{
            "id": "is_inventory",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is inventory available in your desired peering location?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
		},{
			"id": "peer_location",
			"visibility": "is_inventory == No",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Which peering location is you interested in?",
			"watermarkText": "",
			"required": false
		},{
			"id": "problem_start_time",
			"order": 4,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": []
		}
	],
  "$schema": "SelfHelpContent"
}
---
