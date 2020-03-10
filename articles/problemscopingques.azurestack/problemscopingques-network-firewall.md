<properties
    pageTitle="Azure Stack Network for User Environment"
    description="Azure Stack Network for User Environment"
    authors="genlin"
    ms.author="prchint"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629211,32629213,32629223,32629230,32629231,32629277,32629281"
    productPesIds="16226"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="8ccb2fde-2000-4e97-b711-4b07ac45db50"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Azure Stack Network for User Environment
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Stack Environment Details",
    "fileAttachmentHint": "To help the support agent identify your issue, please collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and/or Azure Stack seed ring logs by following the steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
    "formElements": [
        {
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
                    "value": "1910",
                    "text": "1910"
                },
                {
                    "value": "1908",
                    "text": "1908"
                },
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
        },
        {
            "id": "tenant_all_single",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Does the issue occur in a specific tenant or all tenants? ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "All tenants",
                    "text": "All tenants"
                },
                {
                    "value": "Single tenant",
                    "text": "Single tenant"
                }
            ],
            "required": false
        },
        {
            "id": "Subscription_name",
            "order": 7,
             "visibility": "tenant_all_single == Single tenant",
            "controlType": "textbox",
            "displayLabel": "Tenant ID",
            "watermarkText": "ID of the tenant",
            "required": false
        },
        {
          "id": "check_firewall",
            "order": 8,
            "controlType": "dropdown",
            "visibility": "tenant_all_single == Single tenant",
            "displayLabel": "Does the issue occur in a certain resource group or virtual network? ",
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
        },
        {
            "id": "rg_vnet_name",
            "order": 9,
              "visibility": "check_firewall == Yes",
            "controlType": "textbox",
            "displayLabel": " What is the name of resource group or virtual network?",
            "watermarkText": "Name of the resource group or virtual network ",
            "required": false
        },
    {
          "id": "has_worked",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Has this ever worked?",
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
        },
        {
            "id": "error_message",
            "order": 12,
            "visibility": "has_worked == No",
            "controlType": "textbox",
            "displayLabel": "What is the error message?",
           "watermarkText": "Provide the error message you received if any",
             "required": true
        },
        {
            "id": "problem_start_time",
            "order": 900,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
