<properties
	pageTitle="Liftr Datadog"
	description="Liftr Datadog"
	authors="RashmiAn"
	ms.author="rashmia"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32755765,32755769,32755771,32755783,32755774,32755777,32755781,32755786"
    productPesIds="17363"
	cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="355a02de-7be5-11eb-9439-0242ac130002"
	schemaVersion="1"
	ownershipId="PartnerSolutions_Confluent"
/>
# Datadog on Azure
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Datadog on Azure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "correlation_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Correlation ID",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "tenant_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Customer's Tenant ID",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "subscription_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Customer's Subscription ID",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "resource_id",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Customer's Azure Resource ID",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "email_address",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Customer's Email",
            "useAsAdditionalDetails": false,
            "required": false
        },

        {
            "id": "customer_impact",
            "order": 8,
            "controlType": "dropdownlist",
            "displayLabel": "How many customers are impacted by this issue?",
            "watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Just One",
					"text": "Just one"
				}, {
					"value": "More than one but not all",
					"text": "More than one but not all"
				}, {
					"value": "All customers",
					"text": "All customers"
				},  {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": true
		}, 

        
        
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ]
}

