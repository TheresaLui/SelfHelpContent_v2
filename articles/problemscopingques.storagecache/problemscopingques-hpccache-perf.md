<properties
	pageTitle="HPC Cache Performance Issues"
	description="Performance Issues"
	authors="jbut"
	ms.author="jebutl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32674487"
	productPesIds="16790"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="d0924c99-0995-48e7-9cb3-3ebdd2b78267"
    ownershipId="StorageMediaEdge_HPCCache"
/>
# Performance Issues
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Performance Issues",
    "formElements": [{
        "id": "hpc_cache_id",
        "order": 1,
        "controlType": "dropdown",
        "displayLabel": "Please select the HPC Cache that has performance problems",
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
        "id": "hpc_cache_expected_performance",
        "order": 3,
        "controlType": "multilinetextbox",
        "displayLabel": "Expected Performance",
        "watermarkText": "Describe expected performance",
        "required": false,
        "useAsAdditionalDetails": false
    }, {
        "id": "hpc_cache_env_changes",
        "order": 4,
        "controlType": "multilinetextbox",
        "displayLabel": "Changes to Deployment",
        "watermarkText": "Describe any recent changes that you made to your deployment or environment that may be responsible for the performance issues.",
        "required": false,
        "useAsAdditionalDetails": false
    }, {
        "id": "hpc_cache_single_client",
        "order": 5,
        "controlType": "dropdown",
        "displayLabel": "Is this performance problem related to a single client?",
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
        "id": "hpc_cache_client_rg",
        "order": 6,
        "controlType": "dropdown",
        "displayLabel": "Please select the resource group for the problematic client",
        "watermarkText": "Choose an option",
        "required": false,
        "visibility": "hpc_cache_single_client == Yes",
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2019-05-01",
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
        "id": "hpc_cache_client_id",
        "order": 7,
        "controlType": "dropdown",
        "displayLabel": "Please select the problematic client",
        "watermarkText": "Choose an option",
        "required": false,
        "visibility": "hpc_cache_client_rg != null && hpc_cache_client_rg != dont_know_answer",
        "dynamicDropdownOptions": {
            "dependsOn": "hpc_cache_client_rg",
            "uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.Compute/virtualMachines?api-version=2019-07-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "textTemplate": "{name}",
            "valueProperty": "id",
            "textPropertyRegex": "[^/]+$",
            "valuePropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, Don't Know or Not Applicable"
            }
        }
    }, {
        "id": "hpc_cache_workload_description",
        "order": 8,
        "controlType": "multilinetextbox",
        "displayLabel": "Workload Description",
        "watermarkText": "Describe your workload as best as possible",
        "required": true,
        "useAsAdditionalDetails": false,
        "infoBalloonText": "Is it read-heavy, write-heavy, a mix of read and write, or metadata heavy? Approximately how large is the data set that is being accessed? Are the files generally small or large?"
    }, {
        "id": "problem_description",
        "order": 9,
        "controlType": "multilinetextbox",
        "displayLabel": "Additional Details",
        "watermarkText": "Provide additional information about your issue",
        "required": true,
        "useAsAdditionalDetails": true
    }, {
        "id": "problem_start_time",
        "order": 10,
        "controlType": "datetimepicker",
        "displayLabel": "When did the problem start?",
        "required": true
    }]
}
---
