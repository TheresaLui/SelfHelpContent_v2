<properties
	pageTitle="Cannot Connect to or from Internet"
	description="Cannot Connect to or from Internet"
	authors="ritup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32584250"
	productPesIds="15526"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="8766b9f2-62d3-4dc0-8b81-597d2b0535ed"
/>
# Cannot Connect to or from Internet
---
{
    "resourceRequired": true,
    "title": "Cannot Connect to or from Internet",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cannot_connect_vm",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the VM you are experiencing connectivity issues with",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
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
        "id": "problem_vm",
        "order": 2,
        "controlType": "dropdown",
        "required": true,
        "displayLabel": "Please select the virtual machine that cannot connect to and/or from Internet.",
        "watermarkText": "Choose an option",
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines?api-version=2019-07-01",
            "jTokenPath": "value",
            "textProperty": "name",
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
        "id": "problem_interface",
        "order": 3,
        "controlType": "dropdown",
        "required": true,
        "displayLabel": "Please select the network interface.",
        "watermarkText": "Choose an option",
        "visibility": "problem_vm != null",
        "dynamicDropdownOptions": {
            "dependsOn": "problem_vm",
            "uri": "/subscriptions/{subscriptionId}/resourcegroups/{replaceWithParentValue}/providers/Microsoft.Network/networkInterfaces/?api-version=2019-07-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "textTemplate":"",
            "valueProperty": "id",
             "defaultDropdownOptions": 
            {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            },
            "textPropertyRegex": "[^/]+$",
            "valuePropertyRegex":  "[^/]+$"
            }
        },
        {
            "id": "port_direction",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Please select the port and direction.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HTTP 80 (From VM to Internet)",
                    "text": "HTTP 80 (From VM to Internet)"
                },
                {
                    "value": "HTTP 80 (From Internet to VM))",
                    "text": "HTTP 80 (From Internet to VM))"
                },
                {
                    "value": "HTTPS 443 (From VM to Internet)",
                    "text": "HTTPS 443 (From VM to Internet)"
                },
                {
                    "value": "HTTPS 443 (From Internet to VM)",
                    "text": "HTTPS 443 (From Internet to VM)"
                },
                {
                    "value": "FTP 20 & 21 (From VM to Internet)",
                    "text": "FTP 20 & 21 (From VM to Internet)"
                },
                {
                    "value": "FTP 20 & 21 (From Internet to VM)",
                    "text": "FTP 20 & 21 (From Internet to VM)"
                },
                {
                    "value": "Telnet 23 (From VM to Internet)",
                    "text": "Telnet 23 (From VM to Internet)"
                },
                {
                    "value": "Telnet 23 (From Internet to VM)",
                    "text": "Telnet 23 (From Internet to VM)"
                },
                {
                    "value": "DNS 53 (From VM to Internet)",
                    "text": "DNS 53 (From VM to Internet)"
                },  
                {
                    "value": "DNS 53 (From Internet to VM)",
                    "text": "DNS 53 (From Internet to VM)"
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
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": false,
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
