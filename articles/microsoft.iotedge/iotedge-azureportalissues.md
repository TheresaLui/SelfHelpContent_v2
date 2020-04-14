<properties
	pageTitle="Problems related to the Azure portal"
	description="Problems related to the Azure portal"
	service="microsoft.devices"
	resource="iotedge"
	authors="veyalla,kgremban"
	ms.author="veyalla,kgremban"
	selfHelpType="generic"
	supportTopicIds="32680939"
	resourceTags=""
	productPesIds="16509"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="8e8e3fc4-c61c-4cf6-a84b-0d2458e87c56"
	ownershipId="AzureIot_IotEdge"
/>

# Problems related to the Azure portal

## **Recommended Steps**

### **Cloud image with a single blue raindrop**

If you see a cloud image with a single blue raindrop, this happens when partially cached version of page is being rendered in the browser. 

1. Use InPrivate or Incognito mode in your browser
1. Try clearing browser cache and cookies, then refresh the page
1. Try restarting the browser

### **"An error occurred while submitting. Please try again." on Deployment creation**

You create a new deployment, the validations passes, but you see: "An error occurred while submitting. Please try again."

In the text box that shows the deployment to be submitted, search for "properties.desired". If you see one or more module with duplicate "properties.desired" fields, that is the source of the error.

*❌Example of the problem*

```
"ModuleA": {
  "properties.desired": {
    "properties.desired": {
```

A recent change in the portal UI changed how module twin properties are set in a deployment. There is now a "Module Twin Property" field and "Module Twin Property Content" field.

1. Select the "Modules" tab.
1. Select the Module which had duplicate "properties.desired".
1. Check that the correct value is set "Module Twin Property" field.
1. Remove "properties.desired" from "Module Twin Property Content" field. Example:

*❌Incorrect*

```
{
  "properties.desired": {
    "property1": "value1",
    "property2": "value2"
    }
}
```

*✅Correct*

```
{
  "property1": "value1",
  "property2": "value2"
}
```

Now you should be able to create the Deployment.
