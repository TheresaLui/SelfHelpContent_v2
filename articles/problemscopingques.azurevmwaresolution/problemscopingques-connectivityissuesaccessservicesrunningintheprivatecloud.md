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
            "displayLabel": "Where is the source machine located?",
            "watermarkText": "Choose a topology",
            "dropdownOptions": [
                {
                    "value": "Connectivity issue between Azure VM and SDDC",
                    "text": "Connectivity issue between Azure VM and SDDC"
                },
                {
                    "value": "On-Premise connectivity issue (uses S2S GW in vWAN)",
                    "text": "On-Premise connectivity issue (uses S2S GW in vWAN)"
                },
                {
                    "value": "On-Premise connectivity issue (uses Global Reach Express Route)",
                    "text": "On-Premise connectivity issue (uses Global Reach Express Route)"
                },
                {
                    "value": "SDDC VM unable to reach Internet (without Public IP configured)",
                    "text": "SDDC VM unable to reach Internet (without Public IP configured)"
                },
                {
                    "value": "SDDC VM unable to reach Internet (with Public IP configured)",
                    "text": "SDDC VM unable to reach Internet (with Public IP configured)"
                },
                {
                    "value": "Unable to reach SDDC from Internet (DNAT)",
                    "text": "Unable to reach SDDC from Internet (DNAT)"
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
            "displayLabel": "Provide the Resource Group name of the source VM",
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
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{replaceWithParentValue}/providers/Microsoft.Compute/virtualMachines?api-version=2018-05-01",
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
            "visibility": "topology == On-premise, connected to this VNET with ExpressRoute || topology == On-premise, connected to this VNET with VPN Gateway || topology == On-premise, connecting over ExpressRoute and VNET peering || topology==On-premise, connecting over VPN Gateway and VNET peering",
            "controlType": "dropdown",
            "displayLabel": "Chose the virtual network connected to your on-premise network",
            "watermarkText": "Choose a virtual network",
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
            "visibility": "topology == On-Prem connectivity issue (uses S2S GW in vWAN) || topology == On-Prem connectivity issue (uses S2S GW in vWAN)On-Prem connectivity issue (uses Global Reach Express Route)",
            "controlType": "texbox",
            "displayLabel": "What is the IP address of the onprem VM?",
            "watermarkText": "What is the IP address of the onprem VM?",
            "required": true
        },
        {
            "id": "SDDCworkloadIPAddress",
            "order": 8,
            "visibility": "topology == Connectivity issue between Azure VM and SDDC || topology == On-Prem connectivity issue (uses S2S GW in vWAN) || topology == On-Prem connectivity issue (uses Global Reach Express Route) || topology == SDDC VM unable to reach Internet (without Public IP configured) || topology == SDDC VM unable to reach Internet (with Public IP configured)",
            "controlType": "texbox",
            "displayLabel": "What is the SDDC workload IP address?",
            "watermarkText": "What is the SDDC workload IP address?",
            "required": true
        },
        {  
            "id": "IPAddressTroubleConnectingTo",
            "order": 9,
            "visibility": "topology == SDDC VM unable to reach Internet (without Public IP configured) || topology == SDDC VM unable to reach Internet (with Public IP configured)",
            "controlType": "texbox",
            "displayLabel": "What is the Internet IP Address you're having trouble connecting to?",
            "watermarkText": "What is the Internet IP Address you're having trouble connecting to?",
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
            "id": "IPAddressTroubleConnectingTo",
            "order": 11,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "texbox",
            "displayLabel": "Provide the name of the virutal hub",
            "watermarkText": "Provide the name of the virutal hub",
            "required": true
        },
        {  
            "id": "IPAddressTroubleConnectingTo",
            "order": 12,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "texbox",
            "displayLabel": "What is the Public IP you are advertising to the Internet?",
            "watermarkText": "What is the Public IP you are advertising to the Internet?",
            "required": true
        }, 
        {  
            "id": "IPAddressTroubleConnectingTo",
            "order": 13,
            "visibility": "topology == Unable to reach SDDC from Internet (DNAT)",
            "controlType": "texbox",
            "displayLabel": "What is the SDDC IP that is supposed to be mapped to that Public IP?",
            "watermarkText": "What is the SDDC IP that is supposed to be mapped to that Public IP?",
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
