# MagentoSMS
Magento SMS Notification Module by SSLWirireless ISMS API 

||=============================================================================================||
  MagentoSMS Notification Module for variuos Event by SSLWirireless ISMS API Module
||=============================================================================================||

Magento Version: Support Up to Magento ver. 1.9.2.2

Instruction as Following all module are same Step:
 01.Magento_SendIsmsRegister
 02.Magento_SendIsmsOrderPlace
 03.Magento_SendIsmsStatusChange
 04.Magento_SendIsmsShipment


Step01:
 Copy/Upload Module Inner App directory  to Magento Site root folder.
 
Step02: SSLWirireless ISMS API Credential as Follwing Location
		app\code\local\Sslw\Ismsorderplace\Model\Observer.php
		
			$msisdn2='0171767xxxx'; // Store Admin Mobile No
			$sms = 'Your OrderID #'.$incrementId.' & Grand Total# '.$grandTotal.' Thank You @KHIKSHA';//May Change SMS Body here				
			$user ="Zero_Gravity"; [isms.sslwireless.com login user ]
			Password: UserPassword [isms.sslwireless.com login Password]
			$sid = "Stake Holder Name";	 
		

For Developer:
They want to send SMS at 5 places.The places are given bellow with magento event as follow:

	Registration ==customer_register_success Magento Event use
		[/app/code/core/Mage/Customer/controllers/AccountController.php	customer_register_success]
	Order place ==sales_order_place_before Magento Event use
	Delivery ==Customer Will Handle Maually 
	Shipment ==sales_order_shipment_save_after Magento Event use
	confirm and cancel/hold/unhold/processing/compelete  == sales_order_save_after Magento Event use
	
	
Help:
Major Order Status are:
    const STATE_NEW             = 'new';
    const STATE_PENDING_PAYMENT = 'pending_payment';
    const STATE_PROCESSING      = 'processing';
    const STATE_COMPLETE        = 'complete';
    const STATE_CLOSED          = 'closed';
    const STATE_CANCELED        = 'canceled';
    const STATE_HOLDED          = 'holded';
    const STATE_PAYMENT_REVIEW  = 'payment_review';
 


Ref Site:

	https://www.nicksays.co.uk/magento-events-cheat-sheet-1-9/
	http://rabee.me/2014/06/06/Magento-Events-Cheat-Sheet-1-9/
	https://docs.magentocommerce.com/Mage_Sales/Mage_Sales_Model_Order_Shipment.html
	
For More Information Visit:

	Mail US:integration@sslcommerz.com.bd
	http://www.sslwireless.com/product&services.php?id=1
	
	

	
