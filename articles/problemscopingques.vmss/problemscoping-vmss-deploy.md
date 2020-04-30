<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32641072,32641074,32641075,32641076"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0106"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cannot create, update, or scale scale set",
    "fileAttachmentHint": "",
    "diagnosticCard": {
            "title": "Virtual machine scale set diagnostics",
            "description": "These diagnostics will check for details about your selected VM instance within your VMSS.",
            "insightNotAvailableText": "We didn't find any problems"},
    "formElements": [
        {
            "id": "vmss_instance",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "If your issue is related to a specific instance, select the instance name",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/virtualMachines?api-version=2019-03-01",
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
                    "value": "Unable to retrieve list of instances.",
                    "text": "Unable to retrieve list of instances."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "deploy_error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you are getting?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "correlation_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Correlation ID",
            "required": true
        },
        {
            "id": "deployment_operation",
            "order": 4,
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
                    "value": "Scale in or out",
                    "text": "Scale in or out"
                },
                {
                    "value": "Scale up or down",
                    "text": "Scale up or down"
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
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Which of the following describes your scenario?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Add VMs to an existing availability set VMs",
                    "text": "Add VMs to an existing availability set VMs"
                },
                {
                    "value": "Allocation failures for older VM sizes",
                    "text": "Allocation failures for older VM sizes"
                },
                {
                    "value": "VMSS Scaling",
                    "text": "VMSS Scaling"
                }
            ],
            "required": false
        },
        {
            "id": "deployment_manageddisks",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying with managed disks?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "deployment_method",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "How are you deploying your VMSS?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "ARM",
                    "text": "ARM"
                },
                {
                    "value": "Powershell",
                    "text": "Powershell"
                },
                {
                    "value": "CLI",
                    "text": "CLI"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "deployment_from",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to create your VMSS from?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "VHD file",
                    "text": "VHD file"
                },
                {
                    "value": "Snapshot",
                    "text": "Snapshot"
                },
                {
                    "value": "Captured image",
                    "text": "Captured image"
                },
                {
                    "value": "Backup",
                    "text": "Backup"
                }
            ],
            "required": false
        },
        {
            "id": "problem_snapshot_date",
            "order": 9,
            "visibility": "deployment_from == Snapshot",
            "controlType": "datetimepicker",
            "displayLabel": "What was the time of the attempted snapshot?",
            "required": false
        },
        {
            "id": "problem_caputre_date",
            "order": 10,
            "visibility": "deployment_from == Captured image",
            "controlType": "datetimepicker",
            "displayLabel": "What was the time of the image capture?",
            "required": false
        },
        {
            "id": "problem_restore_date",
            "order": 11,
            "visibility": "deployment_from == Backup",
            "controlType": "datetimepicker",
            "displayLabel": "What was the time of the attempted backup?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 12,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 13,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
