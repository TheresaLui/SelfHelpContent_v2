<properties
    pageTitle="Azure Stack Marketplace Management - Download issues"
    description="Azure Stack Marketplace Management - Download issues"
    authors="genlin"
    ms.author="genli"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629186"
    productPesIds="16226"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="8ccb2fde-6f9f-4e97-b711-4b07ac45db50"
/>
# Azure Stack Marketplace Management - Download issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Stack Environment Details",
    "fileAttachmentHint": "To help the support agent identify your issue, please <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-privileged-endpoint'>connect to the Privileged Endpoint</a>, and collect and upload the output of Get-AzureStackStampInformation command",
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
            "id": "registration_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Registration name",
            "watermarkText": "Name of your Azure Stack registration",
            "required": false,
            "infoBalloonText": "You can find the registration name in Region Management - Properties"
        }, {
            "id": "Subscription_name",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Subscription ID",
            "watermarkText": "ID of Azure Subscription used for registration",
            "required": false,
            "infoBalloonText": "You can find the Azure Subscription ID in Region Management- Properties"
        },
{
            "id": "image_name",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Image name",
            "watermarkText": "Image Name",
            "required": false
        },{
            "id": "image_version",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Image version",
            "watermarkText": "Image version",
            "required": false
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