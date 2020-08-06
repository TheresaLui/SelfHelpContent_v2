<properties
	pageTitle="ADFS_Scoping_Questions"
	description="The AD FS scoping question page"
	authors="billmath"
	ms.author="billmath"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32615405,32615362,32615367,32615368,32615375,32615382,32615383,32615427,32615434"
	productPesIds="16579"
	cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="21c79041-b9ae-4f4f-b431-5a3648c97e20"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/>
# AD FS Scoping question
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
	"title": "AD FS Scoping Questions",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "run_diagnostics_analyzer",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Troubleshoot your issue at adfshelp.com/DiagnosticsAnalyzer/Analyze. This automated tool checks common AD FS issues and provides support engineers with your ADFS information, reducing time spent collecting data for your case and help resolving the case faster.",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes, I ran the tool and submitted the diagnostics results to support through AD FS Help."
				}, {
					"value": "No",
					"text": "No, support will collect my diagnostics results in the case."
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": true
		}, {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide details of your AD FS issue, including any error messages, and if applicable attach a screenshot or a file from the Diagnostic Analyzer below.",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Error messages."
				}, {
					"text": "Applicable screenshots."
				}
			]
		}
	]
}
---
