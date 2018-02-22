<properties
	pageTitle="Configure SAP HANA large instances"
	description="Configure SAP HANA large instances"
	authors="phgantik"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32549255,32549257,32549256,32549258,32549259"
	productPesIds="16208,15571,15797"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# SAP HANA LARGE INSTANCES
---
{
	"resourceRequired": false,
	"title": "Configure SAP HANA large instances",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "configure_sap_hana",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Is this an Azure VM or a SAP HANA Large Instance",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Azure VM",
					"text": "Azure VM(G-Series, M-Series,DS-Series etc)"
				},{
					"value": "SAP HANA Large Instance",
					"text": "SAP HANA Large Instance"
				}],
			"required": true
		}, {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "region_sap_hana",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Select the SAP HANA Large Instances Region",
			"dropdownOptions": [{
					"value": "West US",
					"text": "West US"
				}, {
					"value": "East US",
					"text": "East US"
				}, {
					"value": "North Europe",
					"text": "North Europe"
				}, {
					"value": "West Europe",
					"text": "West Europe"
				}, {
					"value": "Australia East",
					"text": "Australia East"
				}, {
					"value": "Australia Southeast",
					"text": "Australia Southeast"
				},
				{
					"value":"other",
					"text":"other"
				}
			],
			"required": true
		}, {
			"id": "large_instance_name",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text":"Names of the SAP HANA Large Instances."
				}, 
				{
					"text":"The IP address of the SAP HANA Large Instance"
				},
				{
					"text":"Note: Make sure you have selected the subscription which contains the SAP HANA Large Instance while creating this case"
				}
			]
		}
	]
}
---
