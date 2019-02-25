<properties
	articleid="vpngwpointtositeconn"
	pageTitle="Point-to-Site VPN connectivity issues information"
	description="Point-to-Site VPN connectivity issues information"
	authors="radwiv"
  ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32591156"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
/>
# Point-to-Site VPN connectivity issues information
---

{   "resourceRequired": false,
    "title": "Point-to-site connectivity issues",
    "fileAttachmentHint": "",
    "formElements": [
        {   "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {   "id": "P2S_connectivity_issues",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you're facing",
            "watermarkText": "Choose an issue",
            "dropdownOptions": [
	          {"value": "Connectionnotestablishing", "text": "Connection not establishing or disconnecting frequently"},
            {"value": "Notreachingdestination", "text": "Not able to reach specific destination"}],
            "required": true
        },
        {   "id": "P2S_connectivity_issues_specificdest",
            "order": 2,
            "visibility": "P2S_connectivity_issues == Notreachingdestination",
            "controlType": "dropdown",
            "displayLabel": "Choose the type of issue",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{"value": "Packet drops", "text": "Packet drops"},
                                {"value": "Throughput", "text": "Throughput"},
                                {"value": "Latency", "text": "Latency"},
                                {"value": "Others", "text": "Others"}],
            "required": true
        },
        {   "id": "source_dest_IP_address",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide source and destination IP addresses",
            "required": false,
            "useAsAdditionalDetails": false,
            "hints": [{"text": "Please provide on-premise and/or VNet IP addresses"}]
        },
        {   "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the device OS",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {"text": "Please provide the device OS (Client platform OS version)"}]
        },
        {   "id": "P2S_tunneltype",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Select the tunnel type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{"value": "SSTP", "text": "SSTP"},
                                {"value": "IPSec", "text": "IPSec"},
                                {"value": "OpenVPN", "text": "OpenVPN"}],
            "required": true
        }
    ]
}
---
