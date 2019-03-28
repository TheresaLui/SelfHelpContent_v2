<properties
	pageTitle="Configure a point-to-site client information"
	description="Configure a point-to-site client information"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwconfigp2sclient"
	supportTopicIds="32633156"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake"
	schemaVersion="1"
/>
# Configure a point-to-site client information
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
       {   "id": "tunnel_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the tunnel type",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{"value": "IKEv2", "text": "IKEv2"},
	    			{"value": "SSTP", "text": "SSTP"},
                                {"value": "OpenVPN", "text": "OpenVPN"}],
            "required": true
        },
        {   "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details including client platform and OS version",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [{"text": "Upload your configuration file to speed up the support process"},
	    	      {"text": "For security purposes, please edit or remove the pre-shared key field from the configuration information"}]
        }
    ]
}
---
