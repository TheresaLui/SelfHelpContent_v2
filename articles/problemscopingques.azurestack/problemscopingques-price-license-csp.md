<properties
    pageTitle="Azure Stack pricing and licensing or partner center usage (for CSPs) questions"
    description="Azure Stack pricing and licensing or partner center usage (for CSPs) questions"
    authors="TobyTu"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629236,32629239"
    productPesIds="16226"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="b4b6273d-558e-4f2d-4872-36a830ea0098"
/>
# Azure Stack pricing and licensing or partner center usage (for CSPs) questions

---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack pricing and licensing or partner center (for CSPs) questions",
      "fileAttachmentHint": "To help the support agent identify your issue, please collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and/or Azure Stack seed ring logs by following the steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
  "formElements": [{
            "id": "hardware_partner",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Azure Stack hardware partner",
            "watermarkText": "Azure Stack OEM Name",
            "dropdownOptions": [
                {
                    "value": "Avanade",
                    "text": "Avanade"
                },
                {
                    "value": "Cisco",
                    "text": "Cisco"
                },
                {
                    "value": "Dell-EMC",
                    "text": "Dell-EMC"
                },
                {
                    "value": "Fujitsu",
                    "text": "Fujitsu"
                },
                {
                    "value": "HPE",
                    "text": "HPE"
                },
                {
                    "value": "Huawei",
                    "text": "Huawei"
                },
                {
                    "value": "Lenovo",
                    "text": "Lenovo"
                },
                {
                    "value": "Terra",
                    "text": "Terra"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Choose the partner or OEM for the hardware your Azure Stack stamp is running on"
        },
        {
            "id": "patch_level",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Current Patch Level",
            "watermarkText": "Example: 1903 if your build number is 1.1903.0.35.",
            "dropdownOptions": [
                {
                    "value": "1907",
                    "text": "1907"
                },
                {
                    "value": "1906",
                    "text": "1906"
                },
                {
                    "value": "1905",
                    "text": "1905"
                },
                {
                    "value": "1904",
                    "text": "1904"
                },
                {
                    "value": "1903",
                    "text": "1903"
                },
                {
                    "value": "1902",
                    "text": "1902"
                },
                {
                    "value": "1901",
                    "text": "1901"
                },
                {
                    "value": "1811",
                    "text": "1811"
                },
                {
                    "value": "1809",
                    "text": "1809"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Example: Select 1903 if your build number is 1.1903.0.35."
        },
        {
            "id": "build_number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Current Build Number",
            "watermarkText": "Example: 1.1903.0.35",
            "required": false,
            "infoBalloonText": "Includes hotfixes. See steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-updates#determine-the-current-version'>Determine the Current Version</a>"
        },
        {
            "id": "region_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },
        {
            "id": "tenant_impact",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Availability of running tenant applications impacted",
            "watermarkText": "Tenant impact",
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
            "required": false,
            "infoBalloonText": "Choose yes if availability of running tenant applications has been impacted"
        },{
            "id": "subscription_registration",
            "order": 6,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the Azure Subscription used for registration?",
            "watermarkText": "Navigate to Azure Stack Region management, then click Properties",
            "infoBalloonText": "Navigate to Azure Stack Region management, then click Properties",
            "required": false
		}, {
            "id": "alert_name",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What is your billing model?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Capacity",
                    "text": "Capacity"
                },
                {
                    "value": "Pay-as-you-use",
                    "text": "Pay-as-you-use"
                }
        ],
            "required": false
        }, {
			"id": "problem_start_time",
			"order": 8,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 9,
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