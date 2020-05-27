<properties
	pageTitle="On-premises device configuration script issues"
	description="On-premises device configuration script issues"
	authors="radwiv"
 	ms.author="radwiv"
	selfHelpType="problemScopingQuestions"
	articleid="vpngwonpremdeviceconfig"
	supportTopicIds="32633159"
	productPesIds="16094"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# On-premises device configuration script issues information
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "On-premises device configuration script issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the type of issue",
            "watermarkText": "Issue type",
            "dropdownOptions": [
                {
                    "value": "script_download",
                    "text": "Issue in downloading the script"
                },
                {
                    "value": "script_installation",
                    "text": "Issue in installing the script"
                },
                {
                    "value": "not_supported",
                    "text": "My device is not supported"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other issues"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Upload your configuration file to speed up the support process (for security purposes, please edit or remove the pre-shared key information)"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
