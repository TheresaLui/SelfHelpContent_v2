<properties
	  pageTitle="Solution for Floating IP Enabled."
	  description="Solution for Floating IP Enabled."
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
	  articleId="bcf9ced6-5386-4be6-905b-0c81d42e4f41"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution for Floating IP Enabled.

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer backend pool connectivity issue. We have reviewed the logs and diagnostics available to us and we determined the connectivity issue you are experiencing may be the result of specifying floating IP on your load balancing rule. Backend connectivity may not work if your VM is not configured to accept connections for the frontend IP address of your load balancing rule. Typically, this is done in conjunction with a clustering technology such as Windows Clustering or Kubernetes (K8s). You can also do this by configuring a loopback adapter in your OS. For more information, see [this documentation](https://docs.microsoft.com/azure/load-balancer/load-balancer-floating-ip).

Please validate that you have configured your clustering technology correctly or that you have a loopback adapter listening on your front-end IP address. If you do not have a clustering technology or loopback adapter configured, please reconfigure your load balancing rule and disable Floating IP.

Best regards,

<!--/issueDescription-->

