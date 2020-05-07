<properties
    pageTitle="Azure ExpressRoute connectivity to Azure Private, Public, or Dynamic 365 services"
    description="Azure ExpressRoute connectivity to Azure Private, Public, or Dynamic 365 services"
    authors="TobyTu"
    ms.author="Mario.Liu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32627985"
    productPesIds="15480"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="a4b6173d-6354-4f2d-8526-36a830ea0098"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Azure ExpressRoute connectivity to Azure Private, Public, or Dynamic 365 services questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure ExpressRoute connectivity to Azure Private, Public, or Dynamic 365 services",
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
            "id": "source_ip",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Source IP address(es)",
            "watermarkText": "Example: 10.0.0.1",
            "required": false
		},{
            "id": "destination_ip",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Destination IP address(es)",
            "watermarkText": "Example: 10.1.0.2",
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