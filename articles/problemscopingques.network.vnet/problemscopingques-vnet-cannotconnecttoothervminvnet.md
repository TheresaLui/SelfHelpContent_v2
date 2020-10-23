<properties
	pageTitle="Cannot connect to other VM in same VNET"
	description="Cannot connect to other VM in same VNET"
	authors="ritup"
    ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584252"
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="855c0eee-0800-4b92-a5bf-fff3858ca56a"
	ownershipId="CloudNet_VirtualNetwork"
/>
# Cannot connect to another virtual machine in the same VNET
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cannot connect to another virtual machine in the same VNET",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Host-to-Guest Port Scanning",
        "description": "Our VM Port Scanner can help you troubleshoot and solve your problem. Please ensure your VM is on, or the tool won't detect the issue.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "from_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the VM you are connecting from",
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
                    "value": "Unable to get the list of VM's",
                    "text": "Unable to get the list of VM's"
                }
            ],
            "required": false
        },
                {
            "id": "VmName",
            "order": 2,
            "controlType": "dropdown",
            "diagnosticInputRequiredClients": "Portal",
            "displayLabel": "Please select the VM you are connecting to",
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
            "id": "SelectedPorts",
            "order": 3,
            "controlType": "dropdown",
            "diagnosticInputRequiredClients": "Portal",
            "displayLabel": "Select the port number you are unable to reach:",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "20 (FTP Date)",
                    "text": "20 (FTP Date)"
                },
                {
                    "value": "21 (FTP Control)",
                    "text": "21 (FTP Control)"
                },
                {
                    "value": "22 (SSH)",
                    "text": "22 (SSH)"
                },
                {
                    "value": "23 (Telnet)",
                    "text": "23 (Telnet)"
                },
                {
                    "value": "53 (DNS)",
                    "text": "53 (DNS)"
                },
                {
                    "value": "80 (HTTP)",
                    "text": "80 (HTTP)"
                },
                {
                    "value": "88 (Kerberos)",
                    "text": "88 (Kerberos)"
                },
                {
                    "value": "110 (POP3)",
                    "text": "110 (POP3)"
                },
                {
                    "value": "135 (RPC)",
                    "text": "135 (RPC)"
                },
                {
                    "value": "143 (IMAP)",
                    "text": "143 (IMAP)"
                },
                {
                    "value": "179 (BGP)",
                    "text": "179 (BGP)"
                },
                {
                    "value": "389 (LDAP)",
                    "text": "389 (LDAP)"
                },
                {
                    "value": "443 (HTTPS)",
                    "text": "443 (HTTPS)"
                },
                {
                    "value": "445 (SMB)",
                    "text": "445 (SMB)"
                },
                {
                    "value": "587 (Exchange)",
                    "text": "587 (Exchange)"
                },
                {
                    "value": "636 (LDAPS)",
                    "text": "636 (LDAPS)"
                },
                {
                    "value": "1433 (SQL)",
                    "text": "1433 (SQL)"
                },
                {
                    "value": "3389 (RDP)",
                    "text": "3389 (RDP)"
                },
                {
                    "value": "5985 (WinRM HTTP)",
                    "text": "5985 (WinRM HTTP)"
                },
                {
                    "value": "5986 (WinRM HTTPS)",
                    "text": "5986 (WinRM HTTPS)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "DestinationPorts",
            "order": 4,
            "visibility": "SelectedPorts == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please provide the port you are unable to reach",
            "watermarkText": "Enter the port",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Are you able to connect or ping another VM/Resource on the Internet?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
