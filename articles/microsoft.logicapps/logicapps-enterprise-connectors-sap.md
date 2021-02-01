<properties
  pagetitle="Enterprise Connector - SAP"
  service="microsoft.logicapps"
  resource="logicapps"
  ms.author="kawilson"
  selfhelptype="Generic"
  supporttopicids="32742543"
  resourcetags=""
  productpesids="15791"
  cloudenvironments="public,fairfax,usnat,ussec,mooncake"
  articleid="304283a0-eb74-4131-9d70-845ef05e5abc"
  ownershipid="Compute_LogicApps" />
# Enterprise Connector - SAP

The Logic Apps' connector works with SAP's classic releases such as R/3 and ECC systems on-premises or hosted in Azure Virtual Machine. The connector also enables integration with SAP's newer HANA-based SAP systems, such as S/4 HANA, whether they're hosted on-premises or in the cloud. The SAP connector supports message or data integration to and from SAP NetWeaver-based systems through Intermediate Document (IDoc), Business Application Programming Interface (BAPI), or Remote Function Call (RFC).

* Connector documentation: [How to connect to SAP systems from Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector)

## **Recommended Documents**

### Installation

- [SAP Connector Installation](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#prerequisites)
- [Multi-tenant Azure prerequisites](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#multi-tenant-azure-prerequisites) 
- [Integration service environment (ISE) prerequisites](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#integration-service-environment-ise-prerequisites)
- [SNC Secure Network Communications prerequisites](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#secure-network-communications-prerequisites)

### Send messages to SAP
- [How to send messages to SAP](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#send-message-to-sap)
- [XML samples for RFC requests](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#xml-samples-for-rfc-requests)
- [XML samples for BAPI requests](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#xml-samples-for-bapi-requests)
- [XML samples for IDoc requests](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#xml-samples-for-idoc-requests)
- [Generate schemas](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#add-an-sap-action-to-generate-schemas)

### Receive messages from SAP
- [How to receive messages from SAP](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#receive-message-from-sap)

### Architecture and design information for the SAP Connector
- [On-premises data gateway architecture](https://docs.microsoft.com/data-integration/gateway/service-gateway-onprem-indepth)
- [How does the Azure Logic App SAP connector trigger work?](https://www.linkedin.com/pulse/how-does-azure-logic-app-sap-connector-trigger-works-david-burg/)
- [Logic App SAP connector IDoc support – going under the hood](https://www.linkedin.com/pulse/logic-app-sap-connector-idoc-support-going-under-hood-david-burg/)
- [BAPI support in Logic Apps SAP connector](https://www.linkedin.com/pulse/bapi-support-logic-apps-sap-connector-david-burg/)
- [Maximizing throughput calling Azure Logic Apps from SAP](https://www.linkedin.com/pulse/maximizing-throughput-calling-azure-logic-apps-from-sap-david-burg/)
- [SAP and Logic Apps, choose your integration approach](https://www.linkedin.com/pulse/sap-logic-apps-you-choose-your-integration-approach-david-burg/)

### Tips and tricks
- [De-duplicate IDOC transmission](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#avoid-sending-duplicate-idocs)
- [Specify the language for the connection](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#change-language-headers)
- [Large request support](https://docs.microsoft.com/archive/blogs/david_burgs_blog/large-request-upcoming-support-for-azure-logic-app-sap-connector)
- [Sending Flat File IDOC](https://www.linkedin.com/pulse/sending-flat-file-idoc-azure-logic-app-sap-connector-david-burg/)
- [Why does confirming a dummy TID in SAP still return success?](https://www.linkedin.com/pulse/why-does-confirming-dummy-tid-sap-still-returns-success-david-burg/)
- [SAP BAPI transaction and lock patterns via stateful connection](https://www.linkedin.com/pulse/azure-logic-apps-support-sap-bapi-transaction-lock-patterns-burg/)
- [Known issues and limitations](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#known-issues-and-limitations)

## **Recommended Steps**

### Troubleshooting
- [Find extended error logs](https://docs.microsoft.com/azure/logic-apps/logic-apps-using-sap-connector#find-extended-error-logs)
- [Logic App SAP connector all the logs](https://docs.microsoft.com/archive/blogs/david_burgs_blog/logic-app-sap-connector-all-the-logs-to-capture-for-troubleshooting-and-requesting-support)
- [Fix "ERROR: max no of 200 conversations exceeded / CPIC-CALL"](https://www.linkedin.com/pulse/fix-error-max-200-conversations-exceeded-cpic-call-sap-david-burg/)
- [Resolving 'SEGMENT_UNKNOWN' error](https://www.linkedin.com/pulse/resolving-segmentunknown-error-from-sap-azure-logic-apps-david-burg/)
- ["NO_FUNCTION_FOUND" error why it happens and how to fix it](https://www.linkedin.com/pulse/nofunctionfound-error-azure-logic-apps-sap-connector-why-david-burg/)
- [SAP sending IDOC to Logic Apps and reply channel failure](https://www.linkedin.com/pulse/sap-sending-idoc-azure-logic-apps-reply-channel-failure-david-burg/)
- [Troubleshooting SAP configuration for Azure Logic App SAP trigger](https://www.linkedin.com/pulse/troubleshooting-sap-configuration-azure-logic-app-trigger-david-burg/)
