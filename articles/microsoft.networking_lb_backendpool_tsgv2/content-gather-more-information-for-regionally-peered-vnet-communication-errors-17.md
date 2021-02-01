<properties
	  pageTitle="Gather more information for regionally peered Vnet communication errors"
	  description="Gather more information for regionally peered Vnet communication errors"
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
	  articleId="48741924-d1b9-4404-b258-769eb68f7176"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Gather more information for regionally peered Vnet communication errors

Collect more information from the source VM and from the customer. Browse to the source VM resource in ASC. Under Diagnostics, use Test Traffic and test from the source VM IP outbound to the load balancer IP and port. Ensure that the traffic is allowed, and the routing layer rule name starts with RouteTargetVnetPeering_VNET. If the routing rule name is RouteTargetNVA, ask customer to verify their NVA configuration. If the traffic is allowed, click "Result File Links" and save the Process Tuples File in the event the case needs to be escalated.

From the customer side, ask them to collect packet captures. Create a DTM link for the customer. Ask the customer for concurrent packet captures from the source and destination VMs (all backend VMs) while reproducing the issue. When you get the packet captures, check to determine if the source sent the TCP SYN packet and note the ephemeral port. Then check that one of the destinations got the inbound SYN from the client IP and ephemeral port previously noted. Check that the backend VM responded with a SYN/ACK. Lastly, check that the client VM received the SYN/ACK. If you need assistance, engage your TA via [Teams resource engagement recommendations](https://aka.ms/ANPTeamsPostingGuidelines) to reach out to SME resources in the [Load Balancer Teams Channel](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fteams.microsoft.com%2Fl%2Fchannel%2F19%253ac5774cb5dd0649f9a68cc88872281084%2540thread.skype%2FLoad%252520Balancer%252520and%252520Public%252520IPs%252520(Public%252520IP%252520Prefix)%3FgroupId%3Dc3e00ac7-3f76-4350-ba3b-e335a6bbbe21%26tenantId%3D72f988bf-86f1-41af-91ab-2d7cd011db47&data=02%7C01%7CMario.Liu%40microsoft.com%7C4ec52986f7d243ddb41708d80c851f92%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637273113181617839&sdata=1BAjB1CPuT6iDgsMpgtZIPg65eRtk0COM10CSXp9Xto%3D&reserved=0)

