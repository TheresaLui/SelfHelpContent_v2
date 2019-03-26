<properties
	articleid="vpngwsitetositeconn"
	pageTitle="Site-to-Site VPN connectivity issues information"
	description="Site-to-Site VPN connectivity issues information"
	authors="radwiv"
        ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32591158"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
/>
# Site-to-Site VPN connectivity issues information
---
{
    "resourceRequired": false,
    "title": "Site-to-site connectivity issues",
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
            "id": "on_prem_devices",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the device you are using",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "A10 Networks",
                    "text": "A10 Networks"
                },
                {
                    "value": "Allied Telesis",
                    "text": "Allied Telesis"
                },
                {
                    "value": "Barracuda Networks, Inc.",
                    "text": "Barracuda Networks, Inc."
                },
                {
                    "value": "Brocade",
                    "text": "Brocade"
                },
                {
                    "value": "Check Point",
                    "text": "Check Point"
                },
                {
                    "value": "Cisco ASA",
                    "text": "Cisco ASA"
                },
                {
                    "value": "Cisco ASR",
                    "text": "Cisco ASR"
                },
                {
                    "value": "Cisco ISR",
                    "text": "Cisco ISR"
                },
                {
                    "value": "Cisco Meraki - Not Compatible",
                    "text": "Cisco Meraki - Not Compatible"
                },
                {
                    "value": "Citrix",
                    "text": "Citrix"
                },
                {
                    "value": "F5",
                    "text": "F5"
                },
                {
                    "value": "Fortinet",
                    "text": "Fortinet"
                },
                {
                    "value": "Internet Initiative Japan",
                    "text": "Internet Initiative Japan"
                },
                {
                    "value": "Juniper",
                    "text": "Juniper"
                },
                {
                    "value": "Microsoft",
                    "text": "Microsoft"
                },
                {
                    "value": "Open Systems AG",
                    "text": "Open Systems AG"
                },
                {
                    "value": "Palo Alto Networks",
                    "text": "Palo Alto Networks"
                },
                {
                    "value": "ShareTech",
                    "text": "ShareTech"
                },
                {
                    "value": "SonicWall",
                    "text": "SonicWall"
                },
                {
                    "value": "Sophos",
                    "text": "Sophos"
                },
                {
                    "value": "Ubiquiti",
                    "text": "Ubiquiti"
                },
                {
                    "value": "WatchGuard",
                    "text": "WatchGuard"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "S2S_connectivity_issues",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you are facing",
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
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "source_dest_IP_address",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide source and destination IP addresses (on-premise and/or VNet IP addresses)",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "onprem_config_script",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Did you use on-premise device configuration script?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "See <a href='https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-download-vpndevicescript'> here</a> for downloading on-premise device configuration script.",
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
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide device Model and iOS/firmware version",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description"
                },
                {
                    "text": "Make, model and OS version of on-premises VPN device(s) (for example, \\"Cisco ASA 5505 OS version 8.3\\")"
                }
            ]
        }
    ]
}
---
