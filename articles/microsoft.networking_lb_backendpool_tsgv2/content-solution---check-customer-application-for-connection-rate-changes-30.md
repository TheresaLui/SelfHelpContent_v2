<properties
	  pageTitle="Solution - Check customer application for connection rate changes"
	  description="Solution - Check customer application for connection rate changes"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="2b8aaea2-f886-43b0-9037-a86bd4fbb04c"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution - Check customer application for connection rate changes

Sudden changes in SYN/FIN rates indicate application issues. It could be that the backend instances of the customer application crashed and as a result caused the customer?s clients to re-connect at around the same time. The next step is to look into the backend server logs and telemetry for additional information as to what may have caused the disconnections and/or re-connections.

