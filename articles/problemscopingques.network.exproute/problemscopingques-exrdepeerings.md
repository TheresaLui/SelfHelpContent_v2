<properties
    pageTitle="Azure ExpressRoute Peerings"
    description="Azure ExpressRoute Peerings"
    authors="TobyTu"
    ms.author="Mario.Liu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32627993"
    productPesIds="15480"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="a9b6173d-9653-4f2d-8526-36a830ea0098"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Azure ExpressRoute Peerings questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure ExpressRoute Peerings",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "peer_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What Expressroute peering do you use?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure private peering",
                    "text": "Azure private peering"
                },
                {
                    "value": "Microsoft peering",
                    "text": "Microsoft peering"
                },
                {
                    "value": "Azure public peering",
                    "text": "Azure public peering"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },{
            "id": "vnet_name",
            "order": 2,
            "controlType": "textbox",
            "visibility": "peer_type == Azure private peering",
            "displayLabel": "Provide the Virtual Network name",
            "watermarkText": "Example: Myvnet",
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