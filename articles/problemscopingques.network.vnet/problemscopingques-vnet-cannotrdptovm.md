<properties
	pageTitle="Cannot RDP or SSH to VM"
	description="Cannot RDP or SSH to VM"
	authors="ritup"
    ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32547225"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="bd533d79-d3fa-439d-964a-2982e28e8ea5"
	ownershipId="CloudNet_VirtualNetwork"
/>

# Cannot connect to virtual machine using RDP or SSH

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cannot connect to virtual machine using RDP or SSH",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Host-to-Guest Port Scanning",
        "description": "Our VM Port Scanner can help you troubleshoot and solve your problem. Please ensure your VM is on, or the tool won't detect the issue.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "diagnosticInputRequiredClients": "Portal",
            "displayLabel": "Please select the VM you are not able to RDP or SSH to?",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions":
                {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of Virtual Machines",
                    "text": "Unable to get the list of Virtual Machines"
                }
            ],
            "required": true
        },
       {
            "id": "port_number",
            "order": 2,
            "controlType": "dropdown",
            "diagnosticInputRequiredClients": "Portal",
            "displayLabel": "Select the port number you are unable to reach:",
            "watermarkText": "Choose an option",
            "dropdownOptions": [                
                {
                    "value": "22 (SSH)",
                    "text": "22 (SSH)"
                },
                                {
                    "value": "3389 (RDP)",
                    "text": "3389 (RDP)"
                },
                             {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "other_port_number",
            "order": 3,
            "visibility": "port_number == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please provide the port you are unable to reach",
            "watermarkText": "Enter the port",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Are you able to tcping the VM's IP address?"
                },
                {
                    "text": "Are you able to RDP/SSH to other VMs in this VNet?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
