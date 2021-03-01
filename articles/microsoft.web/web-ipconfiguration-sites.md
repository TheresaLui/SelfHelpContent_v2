<properties
  pagetitle="configuration and management/ip configuration&#xD;"
  description="configuration and management/ip configuration"
  service="microsoft.web"
  resource="sites"
  ms.author="shrahman"
  selfhelptype="Generic"
  supporttopicids="32542210"
  resourcetags=""
  productpesids="14748,16170"
  cloudenvironments="public,mooncake,fairfax,usnat,ussec,blackforest"
  disableclouds=""
  articleid="ce8300ba-4b00-400a-aaa0-946f930e754b"
  ownershipid="Compute_AppService" />
# configuration and management/ip configuration

## **Recommended steps**

### How do I get a reserved or dedicated Inbound IP Address for my Web Site? 
If  you need to configure a dedicated/reserved IP address for inbound calls made to the azure web app site, you will need to install and configure an IP based SSL certificate.  Please note that in order to do this your App Service Plan should be in Basic or higher pricing tier. <br>

### How do I find the outbound IP addresses?  

Follow these steps:

1. Browse to the details of your specific web app using the new Azure portal at `portal.azure.com`
2. Towards the top of the details for your web app, select the **All settings** link.<br>
   This link opens a list of web app information that you can drill into further. 
3. Select **Properties** to get specific details. 
4. In **Properties**, use the icon to the side of the **Outbound IP Addresses** text box to select these addresses. 
5. To copy an address, press **Ctrl+C**.
