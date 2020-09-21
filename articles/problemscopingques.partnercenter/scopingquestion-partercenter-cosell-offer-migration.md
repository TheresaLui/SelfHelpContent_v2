<properties
pageTitle="Partner Center Cosell offer migration"
    description="Partner Center Cosell offer migration"
    authors="felicefan"
    ms.author="v-felice"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32739474,32739473"
    productPesIds="17006"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="sproblemscopingques_partnercenter_cosell_offer_migration"
    clientIds="partnercenter"
    ownershipId="PartnerCenter_Ingestion"
/>
# Partner Center Co-sell offer migration
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "Partner Center Co-sell offer migration",
	"fileAttachmentHint": "Please attach screenshots that show the problem you are having.",
	"formElements": [{
			"id": "offer_type",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Offer Type",
			"watermarkText": "Please select an Offer Type.",
			"dropdownOptions": [
				{
					"value": "Azure Application offer",
					"text": "Azure Application offer"
				},
				{
					"value": "Dynamics 365 Business Central offer",
					"text": "Dynamics 365 Business Central offer"
				},
				{
					"value": "Dynamics 365 for Customer Engagement offer",
					"text": "Dynamics 365 for Customer Engagement offer"
				},
				{
					"value": "Dynamics 365 for Operations offer",
					"text": "Dynamics 365 for Operations offer"
				},
				{
					"value": "SaaS offer",
					"text": "SaaS offer"
				},
			{
				"value": "dont_know_answer",
				"text": "Don't Know"
			}
			],
			"required": true
		},
		{
			"id": "offer_name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Offer Name",
			"watermarkText": "Please provide the offer name.",
			"required": false
		},
		{
			"id": "ocp_solution_id",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "OCP Solution ID",
			"watermarkText": "Please provide the OCP Solution ID.",
			"required": true
		},
		{
			"id": "url_for_marketplace_listing",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "URL for Marketplace listing",
			"watermarkText": "Please enter the URL from Microsoft AppSource or Azure Marketplace.",
			"required": false
		},
		{
			"id": "problem_start_time",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "Start Time",
			"watermarkText": "When did your issue begin?",
			"required": true
		},
		{
         	"id":"problem_description",
         	"order":6,
         	"controlType":"multilinetextbox",
         	"displayLabel":"Problem description",
         	"watermarkText":"Please describe specifically what your question is about.",
         	"useAsAdditionalDetails":true,
         	"required":true
      }
	]
}
---
