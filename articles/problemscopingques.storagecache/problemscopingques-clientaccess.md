<properties
	pageTitle="HPC Cache Client Access Issues"
	description="Client Access Issues"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32674483"
	productPesIds="16790"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="298c2f72-d3a0-44fb-bf1a-a9aa66eafa53"
/>
# HPC Cache Client Access Issues
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Client Access Issues",
    "formElements": [{
        "id": "hpc_cache_id",
        "order": 1,
        "controlType": "dropdown",
        "displayLabel": "Please select the HPC Cache that you have questions about",
        "watermarkText": "Choose an option",
        "required": true,
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.StorageCache/caches?api-version=2019-11-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, Don't Know or Not Applicable"
            }
        }
    }, {
        "id": "avere_client_name_or_ip",
        "order": 2,
        "controlType": "textbox",
        "displayLabel": "Client Name or IP Address",
        "watermarkText": "Name or IP Address",
        "required": false
    }, {
        "id": "avere_client_os",
        "order": 3,
        "controlType": "textbox",
        "displayLabel": "Client OS Type and Version",
        "watermarkText": "Client OS Type and Version",
        "required": false
    }, {
        "id": "avere_client_ever_worked",
        "order": 4,
        "controlType": "dropdown",
        "displayLabel": "Has this client ever been able to access the system?",
        "watermarkText": "Choose an option",
        "required": false,
        "dropdownOptions": [{
            "value": "Yes",
            "text": "Yes"
        }, {
            "value": "No",
            "text": "No"
        }]
    }, {
        "id": "problem_description",
        "order": 5,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 6,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
