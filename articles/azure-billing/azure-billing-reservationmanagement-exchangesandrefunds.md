<properties
	pageTitle="Cancel or change an existing reservation"
	description="Cancel or change an existing reservation"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32593227"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake"
	articleId="0f67df6b-5123-49f6-9ab8-ff5755ec54f4"
	ownershipId="ASMS_Billing"
/>

# Cancel or change an existing reservation

You can cancel or exchange a reserved instance yourself using [Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade). Select the reservation and click on refund or exchange. Please note following:

* You must have owner access on the Reservation Order to exchange or refund. Access to only the Reservation will not let you proceed with refund or exchange. Ask the Reservation Order owner to give you owner access to the Reservation Order
* You can exchange a reservation for another reservation of the same type – there are no penalties on reservation exchange
* You can also refund reservations, up to a total of $50,000 USD in a 12-month rolling window
* Self-service exchange and cancel capability isn't available for US Government Enterprise Agreement customers. Other US Government subscription types including Pay-As-You-Go and CSP are supported

 Learn more : [How return and exchange transactions are processed](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#how-return-and-exchange-transactions-are-processed)<br>
 
 Learn more : [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)

Other questions: [Visit reserved instance docs](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)

### **Exchange an existing reserved instance (Self-service)**

You can exchange a reservation for another reservation of the same type. You can also refund a reservation, up to $50,000 USD per year, if you no longer need it. Self-service exchange and cancel capability isn't available for US Government Enterprise Agreement customers. Other US Government subscription types including Pay-As-You-Go and CSP are supported. You must have owner access on the Reservation Order to exchange or refund an existing reservation.<br>

The following steps will guide on the procedure to complete the transaction

1. Log in to your [Azure portal](https://portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade). Select the reservations that you want to refund and click **Exchange**<br>
2. Select the VM product that you want to purchase and type a quantity. Make sure that the new purchase total is more than the return total [Determine the right size before you purchase](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances#determine-the-right-vm-size-before-you-buy).<br>
3. Review and complete the transaction

### **Refund for a reserved instance**

To refund a reservation, go to **Reservation Details** and click **Refund**

### **Pro-rated refund:**

When you cancel an RI, the prorated amount is calculated based on the lower of the current price of the RI or the purchase price of the RI and by the months remaining. The months remaining will be rounded up to the next month. The termination fee will be applied on the amount to be returned to the customer.
Here’s an example:

* The customer purchases a one-year term RI for $120 in January 1, 2018
* The customer cancels their RI on April 7, 2018, during the fourth month of their one-year term
* The prorated amount returned to the customer will be calculated this way:

    $120 (the price of the term OR the current market price of that RI, whichever is lower) * (12 – 4)/12 = $80<br>
    12% (termination fee) * $80 (prorated amount) = $9.60<br>
    $80 (prorated amount) - $9.60 (fee) = $70.40 (returned to the customer)<br>

## **Recommended Documents**

* [Prepay for Virtual Machines with Azure Reserved VM Instances](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances#cancellations-and-exchanges)<br>
* [Prepay for SUSE software plans from Azure Reservations](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges#cancellation-and-exchanges-not-allowed)<br>
* [Prepay for SQL Database compute resources with Azure SQL Database reserved capacity](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges#cancellation-and-exchanges-not-allowed)<br>
* [Save money on virtual machines with Azure Reserved Instances](https://docs.microsoft.com/azure/billing/billing-save-compute-costs-reservations)<br>
* [Understand how the reserved instance discount is applied](https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges)<br>
* [Understand reserved instance usage for your Pay-As-You-Go subscription](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage)<br>
* [Understand reserved instance usage for your Enterprise enrollment](https://docs.microsoft.com/azure/billing/billing-understand-reserved-instance-usage-ea)<br>
* [Windows software costs not included with reserved instances](https://docs.microsoft.com/azure/billing/billing-reserved-instance-windows-software-costs)<br>
* [Manage reserved instances](https://docs.microsoft.com/azure/billing/billing-manage-reserved-vm-instance)<br>
* [Manage Microsoft Azure reservations on behalf of your customers](https://docs.microsoft.com/partner-center/azure-reservations-manage)<br>
* [Reserved instances in Partner Center Cloud Solution Provider (CSP) program](https://docs.microsoft.com/partner-center/azure-reservations)<br>
* [How return and exchange transactions are processed](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#how-return-and-exchange-transactions-are-processed)<br>
* [Exchange and Refund policies](https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund#exchange-policies)<br>
