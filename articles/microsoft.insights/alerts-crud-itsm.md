<properties
  pagetitle="I have an issue or I don't know how to create, edit or delete an ITSM integration action&#xD;"
  description="I'm trying to create, edit or delete an ITSM integration action but I don't know how to configure it"
  service="microsoft.insights"
  resource="actiongroups"
  ms.author="nolavime"
  selfhelptype="Generic"
  supporttopicids="32739776"
  resourcetags=""
  productpesids="15454"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="alerts-crud-itsm"
  ownershipid="AzureMonitoring_ActionGroup" />
# I have an issue or I don't know how to create, edit or delete an ITSM integration action

The IT Service Management Connector (ITSMC) allows you to connect Azure and a supported IT Service Management (ITSM) product/service.

## **Recommended Steps**

If you are facing issues while trying to setup ITSM, follow these steps to troubleshoot:

* Ensure that [ITSM Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview#adding-the-it-service-management-connector-solution) is installed

* Check the dashboard in order to see if it contains common errors that can be solved by the [dashboard](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-dashboard)

For **Service Now**:
* Ensure that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-1) are in the ITSM solution workspace and check if all the details are correct: URL, Username/Password, Client ID/Client Secret
* Ensure that you correctly defined the [OAuth connection](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-1) in ServiceNow instance
 * Ensure that the [User App](https://store.servicenow.com/sn_appstore_store.do#!/store/application/ab0265b2dbd53200d36cdc50cf961980/1.0.1) for Microsoft Log Analytics integration is installed
 * Ensure that [integration user](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#create-integration-user-role-in-servicenow-app) role for the user app is configured correctly

For **System Center Service Manager**:

* Ensure that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure) are in the ITSM solution workspace and ensure all the details are correct
* Ensure that The Service Manager [Web application](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#create-and-deploy-service-manager-web-app-service) (Web app) is deployed and configured
* Ensure that [Hybrid connection](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#configure-the-hybrid-connection) is created and configured
    
For **Provance**:

* Ensure that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-2) is in the ITSM solution workspace and check if all the details are correct
* Provance App [should be registered with Azure AD](https://docs.microsoft.com/azure/app-service/configure-authentication-provider-aad) and client ID made available
    
For **Cherwell**:

* Ensure that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-3) is in the ITSM solution workspace and verify that all the details are correct
* Ensure that the [Client ID is generated](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#generate-client-id-for-cherwell)


**Recommended Documents**
* [Troubleshooting problems in ITSM Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-troubleshoot-overview)