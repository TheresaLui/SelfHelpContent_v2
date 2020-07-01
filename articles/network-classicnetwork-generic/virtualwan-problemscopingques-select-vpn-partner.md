<properties
    pageTitle="virtualwan-problemscopingques-select-vpn-partner"
    description="Select My Virtual WAN VPN Partner"
    authors="karenhammons"
    ms.author="karenha,reyandap"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640643,32640645,32640655"
    productPesIds="16572"
    articleId="virtualwan-problemscopingques-select-vpn-partner"
    cloudEnvironments="public,mooncake,fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="CloudNet_VirtualWAN"
/>
# Select VPN Device Partner Configure my On Prem Device 
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Virtual WAN On-Premise VPN Device",
    "fileAttachmentHint": "Upload the scrubbed configuration file for your on-premises VPN Device",
    "formElements": [
    	{
	    "id": "name_partner",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the name of your Virtual WAN Partner",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
	    	{
                 	"value": "Barracuda Networks",
                    	"text": "Barracuda Networks"
                },
		{
                    	"value": "Check Point",
                    	"text": "Check Point"
                },
		{
                    	"value": "Citrix",
                    	"text": "Citrix"
                },
		{
                   	"value": "Netfoundry",
                    	"text": "Netfoundry"
		},
		{
			"value": "Palo Alto Networks",
			"text": "Palo Alto Networks"
		},
		{
			"value": "Riverbed Technology",
			"text": "Riverbed Technology"
		},
		{
			"value": "128 Technology",
			"text": "128 Technology"
		},
		{
			"value": "dont_know_answer",
			"text": "Don't know"
		},
		{
			"value": "Not listed",
			"text": "Not listed"
                }
            ],
            "required": true
	},
	{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
	{
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
	},
	{
	    "id": "learn_more_text",
	    "order": 100,
	    "controlType": "infoblock",
	    "content": "<a href='https://docs.microsoft.com/azure/virtual-wan/virtual-wan-locations-partners'>Learn about configuring devices through our partners</a> Not listed? Find details on how to get your partner onboarded."
        }
    ]
}
---
