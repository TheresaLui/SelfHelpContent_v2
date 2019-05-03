<properties
	pageTitle="ADFS_Scoping_Qustions"
	description="The AD FS scoping question page."
	authors="billmath"
	ms.author="billmath"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32615405,32615362,32615367,32615368,32615375,32615382,32615383,32615427,32615434"
	productPesIds="16579"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="21c79041-b9ae-4f4f-b431-5a3648c97e20"
/>
# AD FS Scoping question
---

{
  "subscriptionRequired": true,
  "resourceRequired": false,
	"title": "AD FS Scoping Questions",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "run_diagnostics_analyzer",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Navigate to adfshelp.microsoft.com/DiagnosticsAnalyzer/Analyze and run the Diagnostics Analyzer tool. Has the information been saved and uploaded to support by selecting the “Save Diagnostics” checkbox? This will reduce time spent troubleshooting your case.",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
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
					"text": "Name of the virtual machine(s) in the same subscription that you think is faster than the slow virtual machine."
				}
			]
		}
	]
}
---