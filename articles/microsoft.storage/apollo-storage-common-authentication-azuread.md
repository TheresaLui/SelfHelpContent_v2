<properties
pageTitle="RBAC Authentication Common Solutions"
description="RBAC Authentication Common Solutions"
ms.author="annayak"
displayOrder=""
articleId="rbac_authentication_apollo_common_solutions"
selfHelpType="Apollo"
supportTopicIds="32678715,32679285,32679292,32679299"
productPesIds="15629,16459,16598,16462,16461"
cloudEnvironments="public"
ownershipId="StorageMediaEdge_XStore"
/>


# Troubleshooting authentication and authorization failures using Apollo //Not showcased in the solution

## Troubleshooting Authentication and Authorization failures

Most customers resolved their Azure AD authentication failures, on their own, using the diagnostics, following the articles or watching the video below.

## Chart for Authentication and Authorization failures
:::Section Recommended solutions:::
The following charts can help you to narrow down the time frames when the Authenciation or Authorization failures occurred

<metric>
<name>Transactions</name>
<aggregationType>Total</aggregationType>
<timeSpanType>relative</ timeSpanType >
<timeSpanDuration>1d</timeSpanDuration>
<title>Storage Authentication and Authorization Failure</title>
<client>Portal</client>
</metric>

## Running a few automated checks

<Insight>
<symptomId>StorageFailureTransactionInsight</symptomId>
<executionText>We are running detailed connectivity checks on your VM</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>Seems like all is good!</noResultText>
<client>ASC</client>
<additionalInputsReq>false</additionalInputsReq>
</Insight>


### Input the response from the previous troubleshooter or provide custom data so we can run a deeper analysis for your problem.


<Insight>
<symptomId>StorageFailureTransactionInsight</symptomId>
<executionText>We are running a more detailed connectivity checks on your VM</executionText>
<timeoutText>We stopped the check, as it was taking too long</timeoutText>
<noResultText>Seems like all is good!</noResultText>
<client>ASC</client>
<additionalInputsReq>true</additionalInputsReq>
</Insight>


## Recommended documents

<CommonSolution>
<articleId>0ffe93a2-8388-4727-9601-fbc18fb6ab0c</articleId>
<client>Portal</client>
</CommonSolution>