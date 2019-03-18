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
    "fileAttachmentHint": "Upload your configuration file to speed the support process. For security purposes, please edit or remove the pre-shared key field from the configuration information.",
    "formElements": [
        {   "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {   "id": "P2S_connectivity_issues",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you're facing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
	    {"value": "Connectionnotestablishing", "text": "Connection not establishing or disconnecting frequently"},
            {"value": "Notreachingdestination", "text": "Not able to reach specific destination"},
	    {"value": "Packet drops", "text": "Packet drops"},
            {"value": "Throughput", "text": "Throughput"},
            {"value": "Latency", "text": "Latency"},
            {"value": "Other", "text": "Other"}],
            "required": true
        },
        {   "id": "source_dest_IP_address",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide source and destination IP addresses (on-premise and/ or VNet IP addresses)",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {   "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the device OS",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [{"text": "Issue description"},
	    {"text": "Device OS (Client platform OS version)"}]
        },
        {   "id": "P2S_tunneltype",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Select the tunnel type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{"value": "IKEv2", "text": "IKEv2"},
	    			{"value": "OpenVPN", "text": "OpenVPN"},
				{"value": "SSTP", "text": "SSTP"}],
            "required": true
        }
    ]
}
---
