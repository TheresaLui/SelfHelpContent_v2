<properties
    pageTitle="Access Azure VMware Solution by CloudSimple - Portal" 
    description="Describes how to access VMware Solution by CloudSimple portal from Azure portal"
    infoBubbleText="Problems related to Site-to-Site VPN between on-premises and Private Cloud network, routing issues, new routes configuration"
    ms.service="azure-vmware-cloudsimple"
    authors="dikamath, sharaths-cs" 
    ms.author="dikamath, b-shsury, v-rabmah"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637617"
    resourceTags=""
    productPesIds="16733"
    cloudEnvironments="public" 
    articleId="11ed1924-1269-45f1-9d2c-6175a9bb8d3c"    
/>

# Troubleshooting site-to-site VPN connectivity to CloudSimple 

## **Recommended Steps**

* Check if there are any bandwidth constraints on your on-premises VPN device. <br>
* Check if any firewall or proxy for  blocking or throttling the traffic. <br>
* Check with ISP for sub-optimal paths to the VPN public IP address. <br>
* Check for Service Policy or QoS applied on L3 interface that caps speed or bandwidth. <br>
* Check router or FW for high CPU or memory utilization. <br>
* Check if an asymmetric path over WAN causing slowness or drops. <br>


## **Recommended Documents**

* [Site-to-Site VPN](https://docs.microsoft.com/azure/vmware-cloudsimple/vpn-gateway#set-up-a-site-to-site-vpn-gateway)<br>
