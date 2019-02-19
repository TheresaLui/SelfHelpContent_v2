<properties
	pageTitle="Site-to-Site VPN connectivity issues information"
	description="Site-to-Site VPN connectivity issues information"
	authors="radwiv"
  ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwsitetositeconn"
	supportTopicIds="32591158"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
/>

---
{
    "resourceRequired": false,
    "title": "VPN Gwy On Prem Device",
    "fileAttachmentHint": "Upload your VPN configuration file. Make sure you edit or remove any pre-shared keys or secrets from the file",
    "formElements": [
        {   "id": "on_prem_devices",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Choose the device you are using",
            "watermarkText": "Choose a device",
            "dropdownOptions": [
                {"value": "A10 Networks", "text": "A10 Networks"},
                {"value": "Allied Telesis", "text": "Allied Telesis"},
                {"value": "Barracuda Networks, Inc.", "text": "Barracuda Networks, Inc."},
                {"value": "Brocade", "text": "Brocade"},
                {"value": "Check Point", "text": "Check Point"},
                {"value": "Cisco ASA", "text": "Cisco ASA"},
                {"value": "Cisco ASR", "text": "Cisco ASR"},
                {"value": "Cisco ISR", "text": "Cisco ISR"},
                {"value": "Cisco Meraki - Not Compatible", "text": "Cisco Meraki - Not Compatible"},
                {"value": "Citrix", "text": "Citrix"},
                {"value": "F5", "text": "F5"},
                {"value": "Fortinet", "text": "Fortinet"},
                {"value": "Internet Initiative Japan", "text": "Internet Initiative Japan"},
                {"value": "Juniper", "text": "Juniper"},
                {"value": "Microsoft", "text": "Microsoft"},
                {"value": "Open Systems AG", "text": "Open Systems AG"},
                {"value": "Palo Alto Networks", "text": "Palo Alto Networks"},
                {"value": "ShareTech", "text": "ShareTech"},
                {"value": "SonicWall", "text": "SonicWall"},
                {"value": "Sophos", "text": "Sophos"},
                {"value": "Ubiquiti", "text": "Ubiquiti"},
                {"value": "WatchGuard", "text": "WatchGuard"},
                {"value": "Other - Please Specify", "text": "Other - Please Specify"}],
            "required": true
        },
        {   "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {   "id": "S2S_connectivity_issues",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you're facing",
            "watermarkText": "Choose an issue",
            "dropdownOptions": [
                {"value": "Tunnel not connected or disconnecting frequently", "text": "Tunnel not connected or disconnecting frequently"},
                {"value": "Not able to reach specific destination", "text": "Not able to reach specific destination"}],
            "required": true
        },
        {   "id": "S2S_connectivity_issues_specificdest",
            "order": 4,
            "visibility": "S2S_connectivity_issues == Not able to reach specific destination",
            "controlType": "dropdown",
            "displayLabel": "Is this issue related to Packet drop",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{"value": "Packet drops", "text": "Packet drops"},
                                {"value": "Throughput", "text": "Throughput"},
                                {"value": "Latency", "text": "Latency"},
                                {"value": "Others", "text": "Others"}],       
            "required": true
        },
        {   "id": "source_dest_IP_address",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide source and destination IP addresses",
            "required": false,
            "useAsAdditionalDetails": false,
            "hints": {"text": "Please provide on-premise and/or VNet IP addresses"},
        },    
        {   "id": "onprem_config_script",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Did you use on-premise device configuration script?",
            "watermarkText": "",
            "dropdownOptions": [{"value": "Yes", "text": "Yes"},
                                {"value": "No", "text": "No"}],
            "required": true
        },
        {   "id": "onprem_config_script_yes",
            "order": 7,
            "visibility": "onprem_config_script == Yes",
            "controlType": "multilinetextbox",
            "displayLabel": "Please list the device configuration script used.",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {   "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide device Model and iOS/firmware version",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {"text": "Issue description"},
                {"text": "Make, model and OS version of on-premises VPN device(s) (for example, \"Cisco ASA 5505 OS version 8.3\")"},
                {"text": "Upload your configuration file to speed up the support process (for security purposes, please edit or remove the pre-shared key information)"}]
        }
    ]
}
---
