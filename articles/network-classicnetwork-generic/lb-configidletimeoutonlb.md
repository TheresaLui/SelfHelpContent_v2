<properties
	pageTitle="configure idle timeout on load balancer"
	description="configure idle timeout on load balancer "
	service="microsoft.network"
	resource="loadbalancers"
	authors="radwiv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32588970"
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public"
/>

# configure idle timeout on load balancer
## **Recommended documents**
Defuault timeout for Inbound connection is 4 minutes which can be extended up to 30 mins by [configuring TCP idle timeout settings](https://docs.microsoft.com/azure/load-balancer/load-balancer-tcp-idle-timeout)<br>
Outbound SNAT connections from the Azure VM have idle timeout is 10 mins which cannot be extended without keep-alive messages.<br>
Both the timeouts can be extended by using [keep-alive messages option](https://msdn.microsoft.com/library/system.net.servicepoint.settcpkeepalive%28v=vs.110%29.aspx)<br>
