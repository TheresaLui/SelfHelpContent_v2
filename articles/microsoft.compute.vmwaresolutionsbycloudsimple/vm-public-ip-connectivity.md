<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to inbound traffic through a Public IP address to an application in CloudSimple Private Cloud"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32627556"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public" 
    articleId="af441601-6699-4716-ad0a-5ecf470e35d4"    
/>

# Troubleshooting public ip address network connectivity 

## **Recommended Steps**

* Check if the virtual machine hosting the application is running. <br>
* Check if the virtual machine's IP address, subnet mask or gateway configured correctly. <br>
* If you are using NSX Distributed Firewall in your Private Clouds, check if it blocks access to that virtual machine. <br>
* Check if the virtual machine's operating system firewall rules block the application's required ports. <br>
* Check if there are firewall rules blocking any inbound or outbound traffic. <br>
* Check if the public IP address is mapped to the correct virtual machine. <br>


## **Recommended Documents**

* [Public IP address](https://docs.microsoft.com/azure/vmware-cloudsimple/public-ips)<br>
* [Firewall Rules](https://docs.microsoft.com/azure/vmware-cloudsimple/firewall#firewall-rules)<br>
* [VLANs/Subnets](https://docs.microsoft.com/azure/vmware-cloudsimple/create-vlan-subnet)<br>
