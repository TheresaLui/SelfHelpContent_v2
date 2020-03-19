<properties
    pageTitle="Azure Stack DNS resolution for user environment"
    description="Azure Stack DNS resolution for user environment"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629210"
    productPesIds="16226"
    cloudEnvironments="Public, Fairfax"
    schemaVersion="1"
    articleId="b4b6273d-9542-4f2d-8526-36a830ea0098"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>
# Azure Stack DNS resolution questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack DNS resolution",
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
        },{
            "id": "dns_provider",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Are you using a custom DNS server or Azure-provided (default)?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Custom",
                    "text": "Custom"
                },
                {
                    "value": "Azure-provided (default)",
                    "text": "Azure-provided (default)"
                }
            ],
            "required": false
        },{
            "id": "ip_address",
            "order": 7,
            "visibility": "dns_provider == Custom",
            "controlType": "textbox",
            "displayLabel": "What is the IP address(es) defined?",
            "watermarkText": "Example: 10.1.0.1",
            "required": false
        },{
            "id": "dns_owner",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Are these DNS server(s) owned by you?",
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
        },{
            "id": "dns_location",
            "order": 9,
            "visibility": "dns_owner == Yes",
            "controlType": "textbox",
            "displayLabel": "Where are these DNS server(s) hosted?",
            "watermarkText": "Enter the location",
            "required": false
        },{
            "id": "dns_setting",
            "order": 10,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Is the DNS setting configured for individual Network Interface Card or for the subnet?",
            "watermarkText": "Enter your answer",
            "required": false
        },{
            "id": "resource_access",
            "order": 11,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Are you able to access the resource using IP address directly?",
            "watermarkText": "Enter your answer",
            "required": false
        },{
            "id": "problem_start_time",
            "order": 12,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        }, {
            "id": "problem_description",
            "order": 13,
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
