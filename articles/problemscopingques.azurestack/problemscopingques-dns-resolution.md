<properties
    pageTitle="Azure Stack DNS resolution for user environment"
    description="Azure Stack DNS resolution for user environment"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629210"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-9542-4f2d-8526-36a830ea0098"
/>
# Azure Stack DNS resolution questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack DNS resolution",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "dns_provider",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are you using a custom DNS server or Azure-provided (default)?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Custom",
                    "text": "Custom"
                },
                {
                    "value": "Azure-provided (default)",
                    "text": "Azure-provided (default)"
                }
            ],
            "required": false
        },{
            "id": "ip_address",
            "order": 2,
            "visibility": "dns_provider == Custom",
            "controlType": "textbox",
            "displayLabel": "What is the IP address(es) defined?",
            "watermarkText": "",
            "required": false
		},{
            "id": "dns_owner",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are these DNS server(s) owned by you?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },{
            "id": "dns_location",
            "order": 4,
            "visibility": "dns_owner == Yes",
            "controlType": "textbox",
            "displayLabel": "Where are these DNS server(s) hosted?",
            "watermarkText": "",
            "required": false
		},{
            "id": "dns_setting",
            "order": 5,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Is the DNS setting configured for individual Network Interface Card or for the subnet?",
            "watermarkText": "",
            "required": false
		},{
            "id": "resource_access",
            "order": 6,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Are you able to access the resource using IP address directly?",
            "watermarkText": "",
            "required": false
		},{
			"id": "problem_start_time",
			"order": 7,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 8,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": []
		}
	],
  "$schema": "SelfHelpContent"
}
---