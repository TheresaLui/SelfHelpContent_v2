<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628252"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0032"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Deploy a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "I received an allocation failure",
    "fileAttachmentHint": "",
    "diagnosticCard": {
            "title": "Virtual machine deployment diagnostics",
            "description": "These diagnostics will check for details about your selected deployment failure.",
            "insightNotAvailableText": "We didn't find any problems"},
    "formElements": [
        {
            "id": "resourceGroup",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select resource group for deployment failure",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource groups.",
                    "text": "Unable to retrieve list of resource groups."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "correlationId",
            "order": 2,
            "visibility": "resourceGroup != null && resourceGroup != dont_know_answer",
            "controlType": "dropdown",
            "displayLabel": "Select failed deployment",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourcegroups/{replaceWithParentValue}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                "jTokenPath": "value",
                "textProperty": "properties.timestamp,properties.parameters.location.value,name",
                "textTemplate": "Time:{properties.timestamp} Region:{properties.parameters.location.value} Name:{name}",
                "valueProperty": "properties.correlationId",
                "defaultDropdownOptions": {
                    "value": "Deployment failure not found.",
                    "text": "Deployment failure not found."
                },
                "textPropertyRegex": "[^/]+$",
                "valuePropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of failed deployments.",
                    "text": "Unable to retrieve list of failed deployments."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "deployment_operation",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create",
                    "text": "Create"
                },
                {
                    "value": "Start",
                    "text": "Start"
                },
                {
                    "value": "Resize",
                    "text": "Resize"
                },
                {
                    "value": "Redeploy",
                    "text": "Redeploy"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "deployment_scenario",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which of the following describes your scenario?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Restart partially stopped (deallocated) VMs",
                    "text": "Restart partially stopped (deallocated) VMs"
                },
                {
                    "value": "Resize a VM or add VMs to an existing availability set",
                    "text": "Resize a VM or add VMs to an existing availability set"
                },
                {
                    "value": "Restart fully stopped (deallocated) VMs",
                    "text": "Restart fully stopped (deallocated) VMs"
                },
                {
                    "value": "Allocation failures for older VM sizes",
                    "text": "Allocation failures for older VM sizes"
                }
            ],
            "required": false
        },
        {
            "id": "deployment_isinavailabilitysetzone",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying your VM in an availability set or zone?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
