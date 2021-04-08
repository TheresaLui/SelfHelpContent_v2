<properties
pageTitle="Partner Center Cosell offer migration"
    description="Partner Center Cosell offer migration"
    authors="felicefan"
    ms.author="v-felice"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32739474,32739473,32789682"
    productPesIds="17006"
    cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
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
	"fileAttachmentHint": "Please upload any supporting files (screenshots or error messages) that can help us understand your issue.",
	"formElements": [{
			"id": "offer_type",
			"visibility": null,
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Offer Type",
			"watermarkText": "Please select an Offer Type",
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
					"text": "Don't know"
				}],
			"required": true
		},
		{
			"id": "offer_name",
			"visibility": null,
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Offer or Solution Name",
			"watermarkText": "Please provide the offer/solution name.",
			"required": false
		},
		{
			"id": "ocp_solution_id",
			"visibility": null,
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "OCP Solution ID",
			"watermarkText": "Enter the OCP Solution ID of the existing solution whose status and material you want to retain",
			"required": true
		},
		{
			"id": "url_for_marketplace_listing",
			"visibility": null,
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "URL for Marketplace listing",
			"watermarkText": "Enter the URL for Microsoft AppSource or Azure Marketplace offer that you want the OCP GTM solution to merge to",
			"required": false
		},
		{
			"id": "migration_related_issue",
			"visibility": null,
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Is your issue related to migrating a solution from OCP GTM to commercial marketplace (PC)?",
			"watermarkText": "Please select from the below list",
			"dropdownOptions": [
				{
					"value": "yes",
					"text": "Yes"
				},
				{
					"value": "no",
					"text": "No"
				},
				{
					"value": "dont_know_answer",
					"text": "Not sure"
				}],
				"required": true
		},
		{
			"id":"additional_issue",
			"visibility": "migration_related_issue==yes",
			"order":6,
			"controlType":"multilinetextbox",
			"displayLabel":"Description of the challenge to migrate from OCP GTM",
			"watermarkText":"Please describe the issue you've encoutered, providing as much details as possible",
			"required": false
		},
		{
			"id": "problem_start_time",
			"visibility": null,
			"order": 7,
			"controlType": "datetimepicker",
			"displayLabel": "Start Date",
			"watermarkText": "When did your issue begin?",
			"required": true
		},
		{
         	"id":"problem_description",
		"visibility": null,
         	"order":8,
         	"controlType":"multilinetextbox",
         	"displayLabel":"Problem description",
         	"watermarkText":"Please provide any other additional information about your issue",
         	"useAsAdditionalDetails":true,
         	"required":true
		}
		]
		}
---
