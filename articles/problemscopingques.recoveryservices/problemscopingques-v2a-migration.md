<properties
    pageTitle="Scoping questions for migration issues"
    description="Scoping questions for migration issues"
    authors="TobyTu"
    ms.author="aaronmax"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32634425"
    productPesIds="16370"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="2b342a85-2019-4l4f-b7d0-43636992e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Migration Issues
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
                    "value": "Migration of VMs to Azure",
                    "text": "Migration of VMs to Azure"
                }, {
					"value": "Migration of an application to Azure",
					"text": "Migration of an application to Azure"
				}, {
					"value": "Migration of Azure resources",
					"text": "Migration of Azure resources"
				}, {
                    "value": "Migration from AWS to Azure",
                    "text": "Migration from AWS to Azure"
                }, {
                    "value": "Migration best practices",
                    "text": "Migration best practices"
                }, {
                    "value": "Unable to boot/RDP after failover",
                    "text": "Unable to boot/RDP after failover"
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
					"value": "Migrate on-premises machines to Azure",
					"text": "Migrate on-premises machines to Azure"
				}, {
					"value": "Best practices for costing and sizing workloads migrated to Azure",
					"text": "Best practices for costing and sizing workloads migrated to Azure"
				}, {
					"value": "Migrate machines after assessment (migrate tool)",
					"text": "Migrate machines after assessment (migrate tool)"
				}, {
					"value": "Azure Migrate - Frequently Asked Questions",
					"text": "Azure Migrate - Frequently Asked Questions"
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