<properties
	pageTitle="VPN client profile issues information"
	description="VPN client profile issues information"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwconfigp2sclient"
	supportTopicIds="32633158"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
/>
# VPN client profile issues information
---
{   "resourceRequired": false,
    "title": "Configure a point-to-site client",
    "fileAttachmentHint": "",
    "formElements": [
        {   "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
       {   "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the type of issue",
            "watermarkText": "",
            "dropdownOptions": [{"value": "profile_download", "text": "Issue in generating or downloading profile"},
                                {"value": "profile_installation", "text": "Issue in installing profile"},
                                {"value": "others", "text": "other issues"}],
            "required": true
        },
        {   "id": "tunnel_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the tunnel type",
            "watermarkText": "",
            "dropdownOptions": [{"value": "SSTP", "text": "SSTP"},
                                {"value": "IPsec", "text": "IPsec"},
                                {"value": "OpenVPN", "text": "OpenVPN"}],
            "required": true
        },
        {   "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details including client platform and OS version",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [{"text": "Upload your configuration file to speed up the support process (for security purposes, please edit or remove the pre-shared key information)"}]
        }
    ]
}
---
