<properties
	pageTitle="Database or elastic pool isn't listed in Azure portal"
	description="Database isn't listed in Azure portal"
	authors="keithelm"
	ms.author="keithelm,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630436,32630437"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="FAD1FE7C-C2A3-408E-8DCA-A3CAE653AD36"
/>
# Availability and Connectivity - Database isn't listed in Azure portal
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
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
            "id": "resource_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of resource is missing?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Please select the resource type that is missing.",
            "dropdownOptions": [
                {
                    "value": "database",
                    "text": "Database"
                },
                {
                    "value": "elastic_pool",
                    "text": "Elastic Pool"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, or don't know answer"
                }
            ],
            "required": true
        },
        {
            "id": "resource_name",
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
            "watermarkText": "Provide additional information about your issue.  Please indicate if the Activity Log shows any recent operations against this resource, such as a rename or delete",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
		      "id": "sqlexception_received_on_client",
			    "order": 2000,
			    "controlType": "multilinetextbox",
    			"displayLabel": "Please provide the verbatim for the SQL error, or client error message you're seeing. Complete callstack (with appropriate user and/or application sensitive information redacted) is preferred.",
		    	"required": false,
			    "visibility": true
	    },
        {
            "id": "database_name",
            "order": 3000,
            "controlType": "dropdown",
            "displayLabel": "Please provide the database name for which you are creating a support ticket.",
            "required": false,
            "infoBalloonText": "Which of these databases are you filing a ticket for?",
            "dynamicDropdownOptions": {
                        "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroup}/providers/Microsoft.Sql/servers/{serverName}/databases?api-version=2017-10-01-preview",
                        "jTokenPath": "value",
                        "textProperty": "properties.description",
                        "valueProperty": "id",
                        "textPropertyRegex": null,
                        "defaultDropdownOptions": {
                                        "value": "dont_know_answer",
                                        "text": "Don't know/None of these"
                                    }
            }
        }
    ]
}
---