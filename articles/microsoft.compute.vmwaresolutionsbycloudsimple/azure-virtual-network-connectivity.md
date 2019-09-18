<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to Azure virtual network connection of a subscription from CloudSimple network, VMware VMs"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637608"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public" 
    articleId="8822e85f-acda-4b67-926c-cc73f52543a5"    
/>

# Troubleshooting Azure virtual network connection 

## **Recommended Steps**

* Check that the Virtual Network Gateway that links to your Azure virtual network to CloudSimple is of type **ExpressRoute**
* Check if a gateway subnet created in the virtual network
* Check if ExpressRoute Gateway already connected to another ExpressRoute circuit in the same peering location
* Check that the correct connection type selected
* Check that the virtual network in the same location as the Virtual Network Gateway
* Check if there is a subnet overlap with the private cloud
* Check if the subnet overlaps with another peered virtual network
* Check if you are linking more than 10 virtual networks in a standard ExpressRoute Circuit


## **Recommended Documents**

* [Azure Virtual Network Connection using ExpressRoute](https://docs.microsoft.com/azure/vmware-cloudsimple/azure-expressroute-connection)<br>



## UI sample
![Microsoft.Common.TextBox](./media/managed-application-elements/microsoft.common.textbox.png)

## Schema
```json
{
  "name": "element1",
  "type": "Microsoft.Common.TextBox",
  "label": "Example text box 1",
  "defaultValue": "my text value",
  "toolTip": "Use only allowed characters",
  "constraints": {
    "required": true,
    "regex": "^[a-z0-9A-Z]{1,30}$",
    "validationMessage": "Only alphanumeric characters are allowed, and the value must be 1-30 characters long."
  },
  "visible": true
}
```