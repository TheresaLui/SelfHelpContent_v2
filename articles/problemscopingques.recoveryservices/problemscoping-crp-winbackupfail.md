<properties
         pageTitle="Scoping questions for Azure VM backup failure for windows"
         description="Scoping questions for Azure VM backup failure for windows"
         authors="srinathvasireddy"
	  ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32637320"
         productPesIds="14749"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="950d1291-6069-4bb8-b439-b817f20deccd"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure VM backup failure for windows
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM backup failure for windows",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Virtual Machine backup failure diagnostics",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Select_ErrorMessage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the error message that you are seeing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "VM Agent is unable to communicate with azure backup service",
                    "text": "VM Agent is unable to communicate with Azure Backup service"
                },
                {
                    "value": "Could not communicate with the VM agent for snapshot status",
                    "text": "Could not communicate with the VM agent for snapshot status"
                },
                {
                    "value": "Snapshot operation failed due to no network connectivity on the virtual machine",
                    "text": " Snapshot operation failed due to no network connectivity on the virtual machine"
                },
                {
                    "value": "Could not copy the snapshot of the virtual machine...",
                    "text": "Could not copy the snapshot of the virtual machine...."
                },
                {
                    "value": "Could not communicate with the VM agent for snapshot status",
                    "text": "Could not communicate with the VM agent for snapshot status"
                },
                {
                    "value": "VM is in Failed Provisioning State",
                    "text": "VM is in Failed Provisioning State"
                },
                {
                    "value": "Currently Azure Backup does not support disk sizes greater than 1023GB",
                    "text": "Currently Azure Backup does not support disk sizes greater than 1023GB"
                },
                {
                    "value": "My error message is not listed here",
                    "text": "My error message is not listed here"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
            "dropdownOptions": [
                {
                    "value": "VM Agent (WA Agent) has latest version",
                    "text": "VM Agent (WA Agent) has latest version"
                },
                {
                    "value": "VM OS version is supported",
                    "text": "VM OS version is supported"
                },
                {
                    "value": "VM has Internet connectivity",
                    "text": "VM has Internet connectivity"
                },
                {
                    "value": "Vault is upgraded to new vault stack V2",
                    "text": "Vault is upgraded to new vault stack V2"
                },
                {
                    "value": "Another backup service is not running",
                    "text": "Another backup service is not running"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
