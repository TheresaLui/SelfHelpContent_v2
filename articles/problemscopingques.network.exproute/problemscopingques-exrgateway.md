<properties
    pageTitle="Azure ExpressRoute Gateway"
    description="Azure ExpressRoute Gateway"
    authors="TobyTu"
    ms.author="Mario.Liu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32627977"
    productPesIds="15480"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b4b6273d-8527-4f2d-8526-36a830ea0098"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Azure ExpressRoute Gateway questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure ExpressRoute Gateway",
  "fileAttachmentHint": "",
  "formElements": [{
        "id": "express_gateway",
        "order": 1,
        "controlType": "dropdown",
        "required": false,
        "displayLabel": "Select the affected Gateway",
        "watermarkText": "Choose an option",
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Network/virtualNetworkGateways?api-version=2019-02-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
        }
          }, {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 3,
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