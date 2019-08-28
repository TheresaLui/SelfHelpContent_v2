<properties
	articleId="FAD1FE7C-C2A3-408E-8DCA-A3CAE653AD36"
	pageTitle="Database isn't listed in Azure portal"
	description="Database isn't listed in Azure portal"
	authors="keithelm"
	ms.author="keithelm,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630436"
	productPesIds="13491"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Availability and Connectivity - Database isn't listed in Azure portal
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Database isn't listed in Azure portal",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "missing_resource_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of resource is missing?",
            "dropdownOptions": [
		{
			"value": "database"
			"text": "Database"
		},
		{
			"value": "elastic_pool"
			"text": "Elastic Pool"
		},
		{
			"value": "dont_know_answer"
			"text": "Other, or don't know answer"
		}
            ]
            "required": true
        },
        {
            "id": "missing_resource_name",
            "order": 10,
            "controlType": "textbox",
            "displayLabel": "Missing Resource Name",
            "watermarkText": "Enter the name of the resource that you expected to see listed.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---