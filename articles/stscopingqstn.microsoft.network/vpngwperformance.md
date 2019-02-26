<properties
	pageTitle="performance"
	description="performance"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwperformance"
	supportTopicIds="32591147"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
/>
# Performance issues information
---
{   "resourceRequired": false,
    "title": "Performance",
    "fileAttachmentHint": "",
    "formElements": [
        {   "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {   "id": "Performance_issues",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the issue you're facing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
	          {"value": "Tunnel not connected or disconnecting frequently", "text": "Tunnel not connected or disconnecting frequently"},
            {"value": "Notreachingdestination", "text": "Not able to reach specific destination"},
            {"value": "Packet drops", "text": "Packet drops"},
            {"value": "Throughput", "text": "Throughput"},
            {"value": "Latency", "text": "Latency"},
            {"value": "Others", "text": "Others"}],
            "required": true
        },
        {   "id": "source_dest_IP_address",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide source and destination IP addresses (on-premise and/or VNet IP addresses)",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {   "id": "onprem_config_script",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Did you use on-premise device configuration script?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{"value": "Yes", "text": "Yes"},
                                {"value": "No", "text": "No"}],
            "required": true
        },
        {   "id": "onprem_config_script_yes",
            "order": 5,
            "visibility": "onprem_config_script == Yes",
            "controlType": "textbox",
            "displayLabel": "Please list the device configuration script used",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {   "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide device Model and iOS/firmware version",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {"text": "Issue description"},
                {"text": "Make, model and OS version of on-premises VPN device(s) (for example, \"Cisco ASA 5505 OS version 8.3\")"},
                {"text": "Upload your configuration file to speed up the support process (for security purposes, please edit or remove the pre-shared key information)"}]
        }
    ]
}
---
