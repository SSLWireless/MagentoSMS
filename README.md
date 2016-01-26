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
	Order place ==sales_order_place_before Magento Event use
	Delivery ==Customer Will Handle Maually 
	Shipment ==sales_order_shipment_save_after Magento Event use
	confirm and cancel/hold/unhold/processing/compelete  == sales_order_save_after Magento Event use
	
For More Information Visit:
http://www.sslwireless.com/product&services.php?id=1

	
