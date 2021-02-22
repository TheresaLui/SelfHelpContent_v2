<properties
	pageTitle="Dynamic Scoping Question URI Contract"
	description="Definition of URI contract for dynamic scoping questions"
	ms.author="bhsurend"
	selfHelpType="problemScopingQuestions"
	supportTopicIds=""
	productPesIds="17001"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="b3232dfd-6033-4e85-8c01-1eae9b8f8e80"
	ownershipId="PartnerCenter_Analytics"
/>
# Useful Title
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Slow virtual machine",
	"fileAttachmentHint": "",
	"formElements": [{
		"id": "ticket_list_relative_path_true",
		"order": 1,
		"controlType": "dropdown",
		"displayLabel": "Please select ticket created?",
		"watermarkText": "Choose an option",
		"dynamicDropdownOptions": {
			"uri": "path:/v1/servicerequests; relative:true",
			"jTokenPath": "items",
			"textProperty": "text",
			"valueProperty": "value",
			"textPropertyRegex": "[^/]+$",
			"defaultDropdownOptions": {
				"value": "dont_know_answer",
				"text": "Other, don't know or not applicable"
			}
		}
	},
	{
		"id": "ticket_list_relative_path_false",
		"order": 2,
		"controlType": "dropdown",
		"displayLabel": "Please select ticket created?",
		"watermarkText": "Choose an option",
		"dynamicDropdownOptions": {
			"uri": "path:'Actual full APIM path here/v1/servicerequests'; relative:false",
			"jTokenPath": "items",
			"textProperty": "text",
			"valueProperty": "value",
			"textPropertyRegex": "[^/]+$",
			"defaultDropdownOptions": {
				"value": "dont_know_answer",
				"text": "Other, don't know or not applicable"
			}
		}
	},
	{
        "id": "problem_start_time",
        "order": 3,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem begin?",
        "required": true
    },
	{
        "id": "problem_description",
        "order": 4,
        "controlType": "multilinetextbox",
        "useAsAdditionalDetails": true,
        "displayLabel": "Details of the issue.",
        "watermarkText": "Provide additional information about your issue including error messages.",
        "required": true
    }]
}
---