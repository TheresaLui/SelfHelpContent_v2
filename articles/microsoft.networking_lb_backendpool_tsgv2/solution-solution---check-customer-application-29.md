<properties
	  pageTitle="Solution - Check customer application"
	  description="Solution - Check customer application"
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
	  articleId="7f461f05-6fa1-4dc8-aff6-2236601aeb91"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Solution - Check customer application

<!--issueDescription-->

Dear <Customer>,

Thank you for contacting us about your load balancer backend pool connectivity issue. We have reviewed diagnostics and configuration available to us and have determined that your connectivity issue is likely due all VMs in your backend pool returning an invalid HTTP response to the load balancer prober address. The next step is to look in your application logs for connections coming from the load balancer probe IP 168.63.129.16.

If you need additional support on this matter, please let us know.  

Best regards,

<!--/issueDescription-->

