<properties
	articleId="problemscopingques-private-link.md"
	pageTitle="Azure Automation - Private Link"
	description="Azure Automation - Private Link"
	authors="bhpat"
	ms.author="bhpat"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32784470"
	productPesIds="15607"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Compute_Automation"
/>
# Azure Automation Private Link 
---
{
    "resourceRequired": true,
	"subscriptionRequired": true,
    "title": "azure automation private link",
    "fileAttachmentHint": "Please provide a screenshot of any errors",
    "formElements": [
	  {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
	        {
            "id": "dns_usage",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Please select the type of DNS usage",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Private DNS Zone",
                    "text": "Azure Private DNS Zone"
                },
                {
                    "value": "Custom DNS",
                    "text": "Custom DNS"
                },
                {
                    "value": "Both",
                    "text": "Both"
                },
                {
                    "value": "Neither",
                    "text": "Neither"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": false
        }
      ,
        {
            "id": "problem_description",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
