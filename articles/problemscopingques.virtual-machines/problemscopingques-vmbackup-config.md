<properties
         pageTitle="Scoping questions for Azure VM configuration protection failure"
         description="Scoping questions for Azure VM configuration protection failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32565494"
         productPesIds="14749"
         cloudEnvironments="public"
         schemaVersion="1"
/>
# Questions Azure VM configuration protection failure
---
{
    "resourceRequired": true,
    "title": "Azure VM configuration failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine is experiencing this problem?",
            "watermarkText": "Enter the name of the virtual machine",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup Job Activity ID",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 3,
            "controlType": "infoblock",
            "content": "Microsoft can provide a solution to your problem faster if you can provide a failed Backup Job Activity ID. From a new browser tab, You can find this from Recovery Services Vault > Monitoring and Report > Backup Jobs > Failed > Activity ID."
        },
        {
            "id": "select_ErrorMessage",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Select the error message that you are seeing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "VM Agent is unable to communicate with azure backup service",
                    "text": " VM Agent is unable to communicate with azure backup service"
                },
                {
                    "value": "Could not communicate with the VM agent for snapshot status",
                    "text": "Could not communicate with the VM agent for snapshot status"
                },
                {
                    "value": "Snapshot operation failed due to no network connectivity on the virtual machine",
                    "text": "Snapshot operation failed due to no network connectivity on the virtual machine"
                },
                {
                    "value": "Could not copy the snapshot of the virtual machine...",
                    "text": "Could not copy the snapshot of the virtual machine..."
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
            "id": "basic_troubleshooting_multiselect",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
            "dropdownOptions": [
                {
                    "value": "VM Agent (WA Agent) is present and has latest version",
                    "text": "VM Agent (WA Agent) has latest version"
                },
                {
                    "value": "VM OS version is supported",
                    "text": "VM OS version is supported"
                },
                {
                    "value": "VM has internet connectivity",
                    "text": "VM has internet connectivity"
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
            "required": true
        },
        {
            "id": "problem_start_date",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
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
