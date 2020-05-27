<properties
	pageTitle="VPN GW Performance"
	description="VPN GW Performance"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwperformance"
	supportTopicIds="32591147,32584880"
	productPesIds="16094,15526"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Performance issues information
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Performance",
    "fileAttachmentHint": "Upload your VPN configuration file. Make sure you edit or remove any pre-shared keys or secrets from the file",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "Performance_issues",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you're facing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Tunnel not connected or disconnecting frequently",
                    "text": "Tunnel not connected or disconnecting frequently"
                },
                {
                    "value": "Notreachingdestination",
                    "text": "Not able to reach specific destination"
                },
                {
                    "value": "Packet drops",
                    "text": "Packet drops"
                },
                {
                    "value": "Throughput",
                    "text": "Throughput"
                },
                {
                    "value": "Latency",
                    "text": "Latency"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "source_dest_IP_address",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide source and destination IP addresses (on-premises and/or VNet IP addresses)",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "onprem_config_script",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Did you use on-premises device configuration script?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "See <a href='https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript'> here</a> for downloading on-premises device configuration script.",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide device Model and iOS/firmware version",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description"
                },
                {
                    "text": "Make, model and OS version of on-premises VPN device(s) (for example, \"Cisco ASA 5505 OS version 8.3\")"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
