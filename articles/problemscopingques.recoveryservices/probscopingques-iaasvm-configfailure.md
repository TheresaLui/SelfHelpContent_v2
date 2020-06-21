<properties
         pageTitle="Scoping questions for Azure VM configuration protection failure"
         description="Scoping questions for Azure VM configuration protection failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553285,32637322"
         productPesIds="15207,15571,15797,16454,16470,14749"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	articleId="4142b082-0f6b-4169-80b3-6f551a623d13"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure VM configuration protection failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM configuration failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which virtual machine is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine",
	    "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
       	    "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": ".*",
	    "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
	    },
            "required": true
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
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "UserErrorGuestAgentStatusUnavailable",
                    "text": "VM Agent is unable to communicate with Azure Backup service"
                },
                {
                    "value": "GuestAgentSnapshotTaskStatusError",
                    "text": "Could not communicate with the VM agent for snapshot status"
                },
                {
                    "value": "ExtensionSnapshotFailedNoNetwork",
                    "text": "Snapshot operation failed due to no network connectivity"
                },
                {
                    "value": "Could not copy the snapshot of the virtual machine",
                    "text": "Could not copy the snapshot of the virtual machine"
                },
                {
                    "value": "UserErrorVmProvisioningStateFailed",
                    "text": "VM is in Failed Provisioning State"
                },
                {
                    "value": "Currently Azure Backup does not support disk sizes greater than 1023GB",
                    "text": "Currently Azure Backup does not support disk sizes greater than 1023GB"
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
            "required": true
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
