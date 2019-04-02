<properties
         pageTitle="Scoping questions for Azure VM backup failure for windows"
         description="Scoping questions for Azure VM backup failure for windows"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553277"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="8a6de52d-409f-4240-ba1c-1bd98e7cc819"
/>
# Questions Azure VM backup failure for windows
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM backup failure for windows",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": true
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
    ]
}
---
