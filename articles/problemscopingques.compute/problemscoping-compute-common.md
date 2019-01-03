<properties
        pageTitle="Problem scoping questions for Cannot Create VM"
        description="This is the scoping question for the VM deployment failure"
        authors="sulama"
        authorAlias="sulama"
        selfHelpType="problemScopingQuestions"
        supportTopicIds="32608639"
        productPesIds="14749"
        cloudEnvironments="Public"
        schemaVersion="1"
        articleId="c1d52907-63c1-4d7e-8fa2-87051c4d1faa"
/>
# Problem with Creating VM
---
{
    "resourceRequired": true,
    "title": "Problem with Creating VM",
    "fileAttachmentHint": "",
    "formElements": [
     	 {
            "id": "resourceGroup",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select Failed Resource Group",
            "watermarkText": "Choose a resource group",
            "content": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [{
						"value": "Unable to retrieve list of resource groups",
						"text": "Unable to retrieve list of resource groups."
					}
					],
            "required": true
        },{
            "id": "correlationId",
            "order": 2,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Select Deployment Failure",
            "watermarkText": "Choose a deployment failure",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourcegroups/{resourceGroup}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "properties.correlationId",
                "textPropertyRegex": "[^/]+$"   
            },
            "dropdownOptions": [{
						"value": "Unable to retrieve list of Deployment Failures",
						"text": "Unable to retrieve list of Deployment Failures."
					}],
            "required": false
        },
	{ 
        "id": "problem_start_time",
        "order": 3, 
        "controlType": "datetimepicker", 
        "displayLabel": "When did the problem begin?", 
        "required": true 
        },{ "id": "problem_description", 
        "order": 4, 
        "controlType": "multilinetextbox", 
        "displayLabel": "Details", 
        "watermarkText": "Provide additional information about your issue", 
        "required": true, 
        "useAsAdditionalDetails": true, 
        "hints": [
            { "text": "Issue description." }, 
            { "text": "Name of the virtual machine(s) in the same subscription that you think is faster than the slow virtual machine."} 
            ] 
       }
    ]
}
---
