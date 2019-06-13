<properties
	pageTitle="Gateway can't start proxy connection to host"
	description="RCA - Gateway can't start proxy connection to host RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="haz"
	ms.author="haz"
	displayOrder="100"
	articleId="dbformariadb-gateway-cannot-start-proxy-connection"
	diagnosticScenario="OrcasMariaDBGatewayCannotStartProxyConneciton"
	selfHelpType="rca"
	supportTopicIds="32640152,32640117,32640118,32640120"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public"
/>

# Gateway can't start proxy connection to host

<!--issueDescription-->
To provide layered security and service scalability connections from clients to your database server are made via a gateway. Our internal service telemetry detected an unusually high number(<!--$Count-->count<!--/$Count-->) of login attempted failures indicating that a gateway process was failing to make a proxy connection to your host database server. Our support engineering team restarted the process and observed connections succeeding as expected. Our engineering team has been made aware of the failed process and will monitor gateways to determine a permanent fix.
<!--/issueDescription-->

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums)
