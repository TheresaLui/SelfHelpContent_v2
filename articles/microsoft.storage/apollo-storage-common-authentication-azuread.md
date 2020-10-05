<properties
pageTitle="RBAC Authentication Common Solutions"
description="RBAC Authentication Common Solutions"
ms.author="annayak"
displayOrder=""
articleId="b7ac8228-62ac-47a7-9427-a8b97fe4f7ca"
selfHelpType="Apollo"
supportTopicIds=""d60f0f12-2be9-1068-02cb-bb9d86b7b6b1,5b03a792-037b-9962-ef13-5c71a55fc5d2,82d8bf7e-861c-910b-b0a7-d647c5ffdf2b,641f6d9b-0cbe-bfb8-3389-7276da029799" 
productPesIds="15629,16459,16598,16462,16461" 
cloudEnvironments="public"
ownershipId="StorageMediaEdge_XStore"
/>

# Troubleshooting authentication and authorization failures using Apollo

## Troubleshooting Authentication and Authorization failures

Most customers resolved their Azure AD authentication failures on their own, using the diagnostics, articles, and video below.

## Chart for Authentication and Authorization failures

:::Section Recommended solutions:::

The following charts can help you to narrow down the time frames when the Authentication or Authorization failures occurred:

<metric>
<name>Transactions</name>
<aggregationType>Total</aggregationType>
<timeSpanType>relative</ timeSpanType >
<timeSpanDuration>1d</timeSpanDuration>
<title>Storage Authentication and Authorization Failure</title>
<client>ASC,Portal</client>
</metric>

## Finding Authentication and Authorization failure occrences 

<Insight>
<symptomId>StorageFailureTransactionInsightLight</symptomId>
<executionText>We are running a quick check to find the authentication or authorization failure occurences on the storage account</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>No authentication or authorization failures were found during the last 24 hours. Please modify the starttime and endtime to choose a different time window.</noResultText>
<client>ASC,Portal</client>
<additionalInputsReq>false</additionalInputsReq>
</Insight>

### Input the response from the previous troubleshooter or provide custom data so we can run a deep analysis on a specific failure

<Insight>
<symptomId>StorageFailureTransactionInsight</symptomId>
<executionText>We are running a detailed analysis on the authentication or authorization</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>Seems like all is good!</noResultText>
<client>ASC,Portal</client>
<additionalInputsReq>true</additionalInputsReq>
</Insight>

<CommonSolution>
<articleId>0ffe93a2-8388-4727-9601-fbc18fb6ab0c</articleId>
<client>Portal</client>
</CommonSolution>
