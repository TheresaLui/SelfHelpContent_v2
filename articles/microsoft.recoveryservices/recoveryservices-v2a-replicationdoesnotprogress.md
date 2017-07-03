<properties
	pageTitle="Site Recovery (VMware to Azure)/Replication does not progress"
	description="Site Recovery (VMware to Azure)/Common issues during replication"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="asgang"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536441"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Site Recovery (VMware to Azure)/Replication does not progress

![replStuck](./ReplicationStuck.jpg)
![seventy](./70percent.jpg)

Customers followed these **[Step-by-Step Troubleshooting instructions](https://blogs.technet.microsoft.com/srinathv/2017/06/28/replication-stuck-replication-not-progressing/)** to resolve Enable Replication issues by
* Fixing connectivity issue between Source Server and Configuration/Process server
* Ensuring Services are up and running  in Source/Process Server
* Ensuring Process Server is able to connect to Azure Public IP address using port 443
* Ensuring IP based firewall on Process Server was not blocking access
* Ensuring URL based firewall on Process Server was not blocking access
* Ensuring Proxy Setting on Process Server was not blocking access
* Ensuring Throttle Bandwidth settings on Process Server was not constraining replication
