<properties
    pageTitle="Azure ExpressRoute performance"
    description="Azure ExpressRoute performance"
    authors="TobyTu"
    ms.author="Mario.Liu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32539947"
    productPesIds="15480"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="a4b6173d-6358-4f2d-8526-36a830ea0098"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Azure ExpressRoute performance questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure ExpressRoute performance",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "source_ip",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Source IP address(es)",
            "watermarkText": "Example: 10.0.0.1",
            "required": false
		},{
            "id": "destination_ip",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Destination IP address(es)",
            "watermarkText": "Example: 10.1.0.2",
            "required": false
		},{
			"id": "problem_start_time",
			"order": 3,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 4,
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