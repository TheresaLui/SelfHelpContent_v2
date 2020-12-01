<properties
	pageTitle="Cannot Connect to or from Internet"
	description="Cannot Connect to or from Internet"
	authors="TobyTu"
        ms.author="mariliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584250"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="8766b9f2-62d3-4dc0-8b81-597d2b0535ed"
	ownershipId="CloudNet_VirtualNetwork"
/>
# Cannot Connect to or from Internet
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cannot Connect to or from Internet",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "VM Connectivity Troubleshooter",
        "description": "Our VM Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "required": true,
            "diagnosticInputRequiredClients": "Portal",
            "displayLabel": "Select the virtual machine you are experiencing connectivity issues with:",
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
                    }
        },
        {
            "id": "traffic_direction",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the traffic direction:",
            "diagnosticInputRequiredClients": "Portal",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "From VM to Internet",
                    "text": "From VM to Internet"
                },
                {
                    "value": "From Internet to VM",
                    "text": "From Internet to VM"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "port_number",
            "order": 3,
            "controlType": "dropdown",
            "diagnosticInputRequiredClients": "Portal",
            "displayLabel": "Select the port number:",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "80 (HTTP)",
                    "text": "80 (HTTP)"
                },
                {
                    "value": "443 (HTTPS)",
                    "text": "443 (HTTPS)"
                },
                {
                    "value": "20 & 21 (FTP)",
                    "text": "20 & 21 (FTP)"
                },
                {
                    "value": "53 (DNS)",
                    "text": "53 (DNS)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide these details:",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Are you trying to connect to or from the internet?"
                },
                {
                    "text": "Are you able to connect or ping another VM in the same VNet?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
