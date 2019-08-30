<properties
    pageTitle="Databricks missing inbound/outbound NSG rules"
    description="DatabrickMissingNetworkSecurityGroupRules"
    infoBubbleText="The following Network Security rules/IP(s) are missing. Inbound Missing Ip Address : {MissingIp}. Outboung Missing Ip Address : {MissingIp}."
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"   
    displayOrder=""
    articleId="Databricks_VNET_MissingNSGRules"
    diagnosticScenario="DatabricksMissingNSGConfigurationInsight"
    selfHelpType="rca"
    supportTopicIds="32677681, 32677679, 32677670, 32677735, 32677711, 32677672, 32677650, 32677676, 32677675"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

Following the inbound network security group rules are missing from network security group <!--$NetworkSecurityGroup-->"ACP-VA7-INT-RG_COMPUTE-DATABRICKS-MCT-NSG"<!--/$NetworkSecurityGroup-->.

## **Recommended Steps**

* Go to the Azure Portal and identify the NSG by name "ACP-VA7-INT-RG_COMPUTE-DATABRICKS-MCT-NSG" that is associated with the public subnet where the cluster is being deployed
* Based on workspace location, We have identifies following missing IP address must be added as “Inbound security rules”. <br/>
Missing IP address : <!--$MissingIp-->23.101.152.95/32 <!--/$MissingIp-->

## **Recommended Documents**

* [Deploy Azure Databricks in your virtual network](https://docs.microsoft.com/en-us/azure/azure-databricks/vnet-injection)
