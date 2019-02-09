<properties
    pageTitle="My Public IP address changed"
    description="My Public IP address changed"
    authors="anavinahar"
    ms.author="anavin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32597608"
    productPesIds="15526"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="752412"
/>

# My public IP address changed

---

{
    "resourceRequired": true,
    "title": "My public IP address changed",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "public_ip_changed",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Please select the virtual machine whose public IP address changed",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/virtualNetworks/{resourcename}/virtualMachines/$ref?api-version=2017-09-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of VM's",
                    "text": "Unable to get the list of VM's"
                }
            ],
            "required": false
        }
    ]
}
---
