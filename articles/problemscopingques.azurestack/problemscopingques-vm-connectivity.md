<properties
    pageTitle="Azure Stack virtual machine connectivity"
    description="Azure Stack virtual machine connectivity"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629202"
    productPesIds="16226"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b4b6273d-9542-4f2d-5238-36a830ea6398"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>
# Azure Stack virtual machine connectivity questions
---
{
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Azure Stack virtual machine connectivity",
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
            "id": "cloud_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the Stamp Cloud ID",
            "watermarkText": "########-####-####-####-###########",
            "infoBalloonText": "Find your <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-find-cloud-id'>Stamp Cloud ID.</a> If you're not sharing diagnostic data or you're running a build earlier than 1910, type N/A.",
            "required": false
        },
        {
            "id": "patch_level",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Current Patch Level",
            "watermarkText": "Example: 2008 if your build number is 1.2008.0.35.",
            "dropdownOptions": [
{
                    "value": "2008",
                    "text": "2008"
                },
                {
                    "value": "2005",
                    "text": "2005"
                },
                {
                    "value": "2002",
                    "text": "2002"
                },
                {
                    "value": "1910",
                    "text": "1910"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Example: Select 2008 if your build number is 1.2008.0.35."
        },
        {
            "id": "build_number",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Current Build Number",
            "watermarkText": "Example: 1.2008.0.35",
            "required": false,
            "infoBalloonText": "Includes hotfixes. Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#determine-the-current-version'>determine the current build number</a>"
        },
        {
            "id": "region_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },
        {
            "id": "tenant_impact",
            "order": 7,
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
            "id": "vm_status",
            "order": 8,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Examine the boot diagnostics and image snapshot, is the VM booted and running?",
            "watermarkText": "Enter your answer",
            "required": false
        },
        {
            "id": "destination_name",
            "order": 9,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the destination URL or IP address and/or port that you are connecting to?",
            "watermarkText": "Enter URL, IP address, port number",
            "required": false
        },
        {
            "id": "connect_name",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "If destination endpoint is within Azure Stack, what are you connecting to?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Private IP address of VM or load balancer (ILB)",
                    "text": "Private IP address of VM or load balancer (ILB)"
                },
                {
                    "value": "Public IP address of VM or load balancer",
                    "text": "Public IP address of VM or load balancer"
                }
            ],
            "required": false
        },
        {
            "id": "connect_method",
            "order": 11,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Are you attempting to connect through S2S tunnel or does the VNet have a Virtual Network Gateway deployed?",
            "watermarkText": "Enter your answer",
            "required": false
        },
        {
            "id": "source_ip",
            "order": 12,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the source IP address that you are attempting to connect from?",
            "watermarkText": "Example: 10.1.0.1",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 13,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 14,
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
