<properties
         pageTitle="Scoping questions for SAP HANA scheduled backup failure"
         description="Scoping questions for SAP Hana scheduled backup failure"
         authors="akanase-ot"
         ms.author="akkanase"
         selfHelpType="problemScopingQuestions"
         supportTopicIds=""
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="e38f8bb3-ce3f-45df-9640-658b7fe57244"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions SAP HANA scheduled backup failure
---
{
	"resourceRequired": true,
	"subscriptionRequired": true,
	"title": "SAP HANA scheduled backup failure",
	"fileAttachmentHint": "",
	"diagnosticCard": {
		"title": "SAP HANA scheduled backup failure",
		"description": "These diagnostics will check for errors.",
		"insightNotAvailableText": "We didn't find any problems"
	},
	"formElements": [{
			"id": "machine_name",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Which machine is experiencing the problem?",
			"watermarkText": "Select the virtual machine running SAP HANA",
			"dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
				"jTokenPath": "value",
				"textProperty": "name",
				"valueProperty": "id",
				"textPropertyRegex": ".*",
				"defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "Other or none of the above"
				}
			},
			"required": false
		},
		{
			"id": "os_version",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the OS version of the machine?",
			"watermarkText": "ex. Windows Server 2012 R2",
			"required": false
		},
		{
			"id": "sap_version",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What is the SAP HANA version and edition?",
			"watermarkText": "ex. SAP HANA 2.0 SPS04",
			"required": false
		},
		{
			"id": "permissions",
			"order": 4,
			"controlType": "dropdown",
            "infoBalloonText": "Info: The script can be found <a href='https://download.microsoft.com/download/B/2/E/B2E01EF8-C247-42A6-BCC7-E45B78F20C99/msawb-plugin-config-com-sap-hana.sh'>here</a>",
			"displayLabel": "Have you run the script available on the Discover DB pane?",
			"watermarkText": "Select",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				},
				{
					"value": "No",
					"text": "No"
				},
				{
					"value": "dont_know_answer",
					"text": "Don’t know"
				}
			],
			"required": false
		},
		{
			"id": "database_Name",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Provide the name(s) of the databases whose scheduled backup is failing?",
			"watermarkText": "Enter database name(s) comma separated",
			"required": false
		},
		{
			"id": "backup_Type",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Is the failure happening during Full/Log/Differential backup?",
			"watermarkText": "Select",
			"dropdownOptions": [{
					"value": "Full backup",
					"text": "Full backup"
				},
				{
					"value": "Log backup",
					"text": "Log backup"
				},
				{
					"value": "Differential backup",
					"text": "Differential backup"
				},
				{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": false
		},
		{
			"id": "jobID_Name",
			"order": 7,
			"controlType": "textbox",
			"displayLabel": "Enter the failed backup job Activity ID",
			"watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
			"required": false
		},
		{
			"id": "error_code",
			"order": 8,
			"controlType": "textbox",
			"displayLabel": "Provide the error code that are you seeing:",
			"infoBalloonText": "Please provide the error code that you are seeing in <a href='https://docs.microsoft.com/azure/backup/sap-hana-db-manage#view-backup-alerts'>Backup alerts</a>.",
			"watermarkText": "Example: UserErrorHanaUnsupportedOperation",
			"required": false
		},
		{
			"id": "basic_troubleshooting_multiselect",
			"order": 9,
			"controlType": "multiselectdropdown",
            "infoBalloonText": "Info: <a href='https://docs.microsoft.com/azure/backup/sap-hana-backup-support-matrix#scenario-support/'>Learn more</a> about the scenarios we support",
			"displayLabel": "Select the troubleshooting steps you have performed:",
			"dropdownOptions": [{
					"value": "Machine has Internet connectivity",
					"text": "Machine has Internet connectivity"
				},
				{
					"value": "NSG/ Proxy is configured and required URLs are whitelisted",
					"text": "NSG/ Proxy is configured and required URLs are whitelisted"
				},
				{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": false
		},
		{
			"id": "problem_start_time",
			"order": 10,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true,
			"diagnosticInputRequiredClients": "Portal"
		},
		{
			"id": "problem_description",
			"order": 11,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Additional details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"hints": []
		}
	],
	"$schema": "SelfHelpContent"
}
---
