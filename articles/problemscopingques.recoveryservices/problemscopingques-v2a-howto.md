<properties
    pageTitle="Scoping questions for how to and general issues"
    description="Scoping questions for how to and general issues"
    authors="TobyTu"
    ms.author="aaronmax"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32630518"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="2b342a85-2019-4l4f-b7d0-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions How-To and General Issues
---
{
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "How-To and General Issues",
  "fileAttachmentHint": "",
  "formElements": [{
            "id": "Select_Question",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "I have a question about:",
            "watermarkText": "Choose a question",
            "dropdownOptions":[{
                    "value": "Protection of application",
                    "text": "Protection of application"
                }, {
					"value": "Migration of an application",
					"text": "Migration of an application"
				}, {
					"value": "New OS, Kernel, configuration support",
					"text": "New OS, Kernel, configuration support"
				}, {
                    "value": "Pricing of Azure Site Recovery",
                    "text": "Pricing of Azure Site Recovery"
                }, {
                    "value": "Azure Site Recovery architecture",
                    "text": "Azure Site Recovery architecture"
                }, {
                    "value": "Replication to storage account",
                    "text": "Replication to storage account"
                }
			],
			"required": false
		}, {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "Basic_troubleshooting_multiselect",
			"order": 3,
			"controlType": "multiselectdropdown",
			"displayLabel": "I have gone through these articles:",
			"dropdownOptions": [{
					"value": "Common questions - VMware to Azure replication",
					"text": "Common questions - VMware to Azure replication"
				}, {
					"value": "What workloads can you protect with Azure Site Recovery?",
					"text": "What workloads can you protect with Azure Site Recovery?"
				}, {
					"value": "VMware VMs and physical servers to Azure support matrix",
					"text": "VMware VMs and physical servers to Azure support matrix"
				}, {
					"value": "Migrate on-premises machines to Azure",
					"text": "Migrate on-premises machines to Azure"
				}, {
					"value": "Other, don't know or not applicable",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 4,
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