<properties
	pageTitle="Azure Defender - Vulnerability Assessment (VA) - Solutions (BYOL)"
	description="Azure Defenderr - Vulnerability Assessment (VA) - Solutions (BYOL)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749421"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_va_byol"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Vulnerability Assessment (VA) - Solutions (BYOL)",
				"subscriptionRequired": false,
                "formElements": [
                {
                    "id": "issue_type",
                    "order": 2,
                    "controlType": "dropdown",
                    "displayLabel": "Please select the issue you are requesting support for",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Failure to provision VA solution",
                            "text": "Failure to provision VA solution"
                        },
                        {
                            "value": "Recommendation to install VA solution is missing",
                            "text": "Recommendation to install VA solution is missing"
                        },
                        {
                            "value": "VA findings missing or not updating",
                            "text": "VA findings missing or not updating"
                        },                     
						{
                            "value": "dont_know_answer",
                            "text": "General Question / Other"
                        }
                    ],
                    "required": true
                },{
                    "id": "autoprov_configured",
                    "order": 3,
                    "controlType": "dropdown",
                    "displayLabel": "Is Auto-Provisioning configured?",
                    "watermarkText": "Choose an option",
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
                            "text": "Other"
                        }
                    ],
                    "required": true
                }{
                    "id": "issue_location",
                    "order": 4,
                    "controlType": "dropdown",
                    "displayLabel": "VM OS Type",
                    "watermarkText": "Choose an option",
                    "dropdownOptions": [
                        {
                            "value": "Microsoft Windows (All versions)",
                            "text": "Microsoft Windows (All versions)"
                        },
                        {
                            "value": "Red Hat",
                            "text": "Red Hat"
                        },
                        {
                            "value": "SuSE",
                            "text": "SuSE"
                        },   
						{
                            "value": "Oracle Enterprise Linux",
                            "text": "Oracle Enterprise Linux"
                        },
                        {
                            "value": "Debian",
                            "text": "Debian"
                        },
                        {
                            "value": "Ubuntu",
                            "text": "Ubuntu"
                        },                        {
                            "value": "dont_know_answer",
                            "text": "Other or Custom Image"
                        }
                    ],
                    "required": true
                },{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
