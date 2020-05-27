<properties
	pageTitle="HPC Cache Installation and Setup"
	description="Installation and Setup"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32674485"
	productPesIds="16790"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="5bd9d665-d737-4bf8-9c7e-7ed4ee509058"
    ownershipId="StorageMediaEdge_HPCCache"
/>
# Installation and Setup
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Installation and Setup",
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
        "id": "hpc_cache_storage_target",
        "order": 2,
        "controlType": "dropdown",
        "displayLabel": "Please select the relevant storage target if applicable",
        "watermarkText": "Choose an option",
        "required": false,
        "visibility": "hpc_cache_id != null && hpc_cache_id != dont_know_answer",
        "dynamicDropdownOptions": {
            "dependsOn": "hpc_cache_id",
            "uri": "{replaceWithParentValue}/storageTargets?api-version=2019-11-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "textTemplate": "{name}",
            "valueProperty": "id",
            "textPropertyRegex": "[^/]+$",
            "valuePropertyRegex": "^+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, Don't Know or Not Applicable"
            }
        }
    }, {
        "id": "problem_description",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Description",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 4,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
