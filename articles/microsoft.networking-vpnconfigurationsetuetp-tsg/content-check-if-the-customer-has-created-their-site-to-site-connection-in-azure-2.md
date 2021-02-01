    <properties
          pageTitle="Check if the customer has created their site-to-site connection in Azure"
          description="Check if the customer has created their site-to-site connection in Azure"
          service="microsoft.network"
          resource="virtualnetworkgateways"
          authors="rimayber"
          ms.author="rimayber"
          displayOrder=""
          selfHelpType="TSG_Content"
          supportTopicIds=""
          resourceTags=""
          productPesIds=""
          cloudEnvironments="public, fairfax, usnat, ussec"
          articleId="f2e10c35-6bec-4bbf-9150-e84347783cf7"
           ownershipId="Centennial_CloudNet_AzureVPNGateway"
    />

    # Check if the customer has created their site-to-site connection in Azure

    The S2S connection object in Azure is required for a working S2S VPN connection

# How to check if the customer has created the connection object
1.  Go to ASC > Resource Explorer > Resource Provider :  Microsoft.Network\Connections
2. Make sure that there is at least one connection that maps to the S2S tunnel with the customer's onprem VPN device

