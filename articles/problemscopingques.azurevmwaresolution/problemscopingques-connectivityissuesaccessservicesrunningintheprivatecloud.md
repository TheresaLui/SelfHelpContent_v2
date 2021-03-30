<properties
	articleId="accessservicesrunninginprivatecloud"
	pageTitle="accessservicesrunninginprivatecloud"
	description="AVS connectivity - access scoping questions"
	authors="neshenoy"
	ms.author="neshenoy"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743018"
	productPesIds="17080"
	cloudEnvironments="Public,FairFax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Azure_VMwareSolution_Content"
/>
# connectivity issue Access services running in the private cloud 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Access services running in the private cloud",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "topology",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What is the topology?",
            "watermarkText": "Choose a topology",
            "dropdownOptions": [
                {
                    "value": "Connectivity issue between Azure VM and SDDC",
                    "text": "Connectivity issue between Azure VM and SDDC"
                },
                {
                    "value": "On-Premises connectivity issue (uses S2S GW in vWAN)",
                    "text": "On-Premise connectivity issue (uses S2S GW in vWAN)"
                },
                {
                    "value": "On-Premise connectivity issue (uses Global Reach Express Route)",
                    "text": "On-Premise connectivity issue (uses Global Reach Express Route)"
                },
                {
                    "value": "SDDC VM unable to reach internet (without public IP configured)",
                    "text": "SDDC VM unable to reach internet (without public IP configured)"
                },
                {
                    "value": "SDDC VM unable to reach internet (with public IP configured)",
                    "text": "SDDC VM unable to reach internet (with public IP configured)"
                },
                {
                    "value": "Unable to reach SDDC from internet (DNAT)",
                    "text": "Unable to reach SDDC from internet (DNAT)"
                },
                {
                    "text": "Other or none of the above",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "resourceGroup",
            "order": 4,
            "visibility": "topology == Connectivity issue between Azure VM and SDDC",
            "controlType": "dropdown",
            "displayLabel": "Provide the Resource Group name of the Azure VM",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource groups",
                    "text": "Unable to retrieve list of resource groups"
                }
            ],
            "required": true
        },
        {
            "id": "VMName",
            "order": 5,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Provide the name of the Azure VM",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.Compute/virtualMachines?api-version=2020-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		"valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of VMs",
                    "text": "Unable to retrieve list of VMs"
                }
            ],
            "required": true
        },
        {
            "id": "HubVNET",
            "order": 6,
            "visibility": "topology == On-premises, connected to this VNET with ExpressRoute || topology == On-premises, connected to this VNET with VPN Gateway || topology == On-premises, connecting over ExpressRoute and VNET peering || topology==On-premises, connecting over VPN Gateway and VNET peering",
            "controlType": "dropdown",
            "displayLabel": "Choose the virtual network connected to your on-premises network",
            "watermarkText": "Virtual network",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Network/virtualNetworks?api-version=2018-05-02",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of VNETs",
                    "text": "Unable to retrieve list of VNETs"
                }
            ],
            "required": true
        },
        {
            "id": "IPAddressOnPremVM",
            "order": 7,
            "visibility": "topology == On-Premises connectivity issue (uses S2S GW in vWAN) || topology == On-Premises connectivity issue (uses S2S GW in vWAN) || topology == On-Premises connectivity issue (uses Global Reach Express Route)",
            "controlType": "textbox",
            "displayLabel": "What is the IP address of the on-premises VM?",
            "required": true
        },
        {
            "id": "SDDCworkloadIPAddress",
            "order": 8,
            "visibility": "topology == Connectivity issue between Azure VM and SDDC || topology == On-Premises connectivity issue (uses S2S GW in vWAN) || topology == On-Premises connectivity issue (uses Global Reach Express Route) || topology == SDDC VM unable to reach Internet (without Public IP configured) || topology == SDDC VM unable to reach Internet (with Public IP configured)",
            "controlType": "textbox",
            "displayLabel": "What is the SDDC workload IP address?",
            "required": true
        },
        {
            "id": "IPAddressTroubleConnectingTo",
            "order": 9,
            "visibility": "topology == SDDC VM unable to reach Internet (without Public IP configured) || topology == SDDC VM unable to reach Internet (with Public IP configured)",
            "controlType": "textbox",
            "displayLabel": "What is the internet IP address you're having trouble connecting to?",
            "required": true
        },
        {
            "id": "resourceGroup1",
            "order": 10,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "dropdown",
            "displayLabel": "Provide the Resource Group name of the virtual hub",
            "watermarkText": "Provide the Resource Group name of the virtual hub",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource groups",
                    "text": "Unable to retrieve list of resource groups"
                }
            ],
            "required": true
        },
        {
            "id": "virtualhub",
            "order": 11,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the virtual hub",
            "required": true
        },
        {
            "id": "PublicIPyouareadvertisingtotheInternet",
            "order": 12,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "textbox",
            "displayLabel": "What is the public IP address you're advertising to the internet?",
            "required": true
        },
        {
            "id": "IPthatissupposedtobemappedtothatPublicIP",
            "order": 13,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "textbox",
            "displayLabel": "What's the SDDC IP that's supposed to be mapped to that public IP?",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 100,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
