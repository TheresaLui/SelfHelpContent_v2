<properties
	  pageTitle="Gather more information for connections from on-premises"
	  description="Gather more information for connections from on-premises"
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
	  articleId="becf2957-9d6f-4f85-9e7b-b09b59cb5603"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Gather more information for connections from on-premises

Collect more information from a backend pool member VM and from the customer. Browse to the backend VM resource in ASC. Under Diagnostics, use Test Traffic and test from the source IP with traffic direction TunnelOrLocalIn. Validate in the result that the "Stateful Test (NSG Layer)" shows that the traffic is allowed. Run Test Traffic again, specifying direction Out, the source IP for the backend DIP, source port 1234, destination IP of the customer's on-premises IP, and destination port 80. The port numbers you choose are not important in this case as we are validating the routing layer and not the stateful/NSG layer as the return traffic will be matched to the inbound flow. Run the test. In the results section, ensure that under "Stateless Test (Routing Layer)" the traffic is allowed and that the rule name begins with RouteTargetVpn_. If the rule name starts with RouteTargetNva, ask the customer to validate the configuration of their network virtual appliance.

From the customer side, ask them to collect a traceroute from their source and copy/paste the result and send it to you. Also ask for packet captures. Create a DTM link for the customer. Ask the customer for concurrent packet captures from the source and destination VMs (all backend VMs) while reproducing the issue. 

When you get the customer?s traceroute, ensure that it gets at least to the VNet ExpressRoute or VPN Gateway CA. If it does not get that far, there could be an on-premises routing problem.

When you get the packet captures, check to determine if the source sent the TCP SYN packet and note the ephemeral port. Then check that one of the destinations got the inbound SYN from the client IP and ephemeral port previously noted. Check that the backend VM responded with a SYN/ACK. Lastly, check that the client VM received the SYN/ACK. If you need assistance, engage your TA via [Teams resource engagement recommendations](https://aka.ms/ANPTeamsPostingGuidelines) to reach out to SME resources in the [Load Balancer Teams Channel](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fteams.microsoft.com%2Fl%2Fchannel%2F19%253ac5774cb5dd0649f9a68cc88872281084%2540thread.skype%2FLoad%252520Balancer%252520and%252520Public%252520IPs%252520(Public%252520IP%252520Prefix)%3FgroupId%3Dc3e00ac7-3f76-4350-ba3b-e335a6bbbe21%26tenantId%3D72f988bf-86f1-41af-91ab-2d7cd011db47&data=02%7C01%7CMario.Liu%40microsoft.com%7C4ec52986f7d243ddb41708d80c851f92%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637273113181617839&sdata=1BAjB1CPuT6iDgsMpgtZIPg65eRtk0COM10CSXp9Xto%3D&reserved=0)

