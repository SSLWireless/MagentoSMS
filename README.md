# MagentoSMS
MagentoSMS NotificationModule by SSLWirireless ISMS API Module

||================================================================================||
  MagentoSMS Notification Module for variuos Event by SSLWirireless ISMS API Module
||================================================================================||

Instruction as follows

Step01:
 Copy/Upload Module Inner App directory  to Magento Site root folder.
 
Step02: SSLWirireless ISMS API Credential as Follwing Location
		app\code\local\Sslw\Ismsorderplace\Model\Observer.php
		
			$msisdn2='0171767xxxx'; // Store Admin Mobile No
			$sms = 'Your OrderID #'.$incrementId.' & Grand Total# '.$grandTotal.' Thank You @KHIKSHA';//May Change SMS Body here				
			$user ="Zero_Gravity"; [isms.sslwireless.com login user ]
			Password: UserPassword [isms.sslwireless.com login Password]
			$sid = "Stake Holder Name";	 
		

[For Developer:
They want to send SMS at 5 places.The places are given bellow with magento event as follow:
		1)Registration ==> customer_register_success Magento Event use
		2)Order place ==>sales_order_place_before Magento Event use
		3)Delivery ==>Customer Will Handle Maually 
		4)Shipment ==>sales_order_shipment_save_after Magento Event use
		5)confirm and cancel/hold/unhold/processing/compelete  ==> sales_order_save_after Magento Event use
		]
