<properties
	pageTitle="HPC Cache My Problem is not Listed"
	description="My Problem is not Listed"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32674486"
	productPesIds="16790"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="a0f174a7-bf33-426e-bf76-f8333fce8130"
    ownershipId="StorageMediaEdge_HPCCache"
/>
# My Problem is not Listed
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "General Guidance or Advisory",
    "formElements": [{
        "id": "hpc_cache_id",
        "order": 1,
        "controlType": "dropdown",
        "displayLabel": "Please select the HPC Cache that you have questions about",
        "watermarkText": "Choose an option",
        "required": false,
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
        "id": "problem_description",
        "order": 2,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 3,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
