


Only Checkout time Registration SMS

app\design\frontend\rwd or base or yourTheme Package \yourThemeName\template\checkout\success.phtml
just add following code:


//Start New Customer Registration SMS Here 			
$customerAddressId = Mage::getSingleton('customer/session')->getCustomer()->getDefaultBilling();

$address = Mage::getModel('customer/address')->load($customerAddressId);

$msisdn = $address->getTelephone();		

$quoteId = $order->getQuoteId();
$quote = Mage::getModel('sales/quote')->load($quoteId);
$method = $quote->getCheckoutMethod(true);
$customer_email = $order->getCustomerEmail();
if ($method == 'register'){ 
//code to handle if customer just registered to your site
//START SMS API Code here your code
$sms = 'Congrats! You have successfully Register using email '.$customer_email.' Thank You.@KHIKSHA';							
$user ="Zero_Gravity";
$pass = "zero123"; 
$sid = "khiksha";	 	
$url = "http://sms.sslwireless.com/pushapi/dynamic/server.php";
$unique_id_1 = uniqid();
$unique_id_2 = uniqid();
$param = "user=$user&pass=$pass&sid=$sid&";
$sms = "sms[0][0]=$msisdn&sms[0][1]=" . urlencode($sms) . "&sms[0][2]=" . $unique_id_1 . "&sms[1][0]=$msisdn2&sms[1][1]=" . urlencode($sms) . "&sms[1][2]=" . $unique_id_2 . "";
$data = $param . $sms . $sid;
$crl = curl_init();
curl_setopt($crl, CURLOPT_SSL_VERIFYPEER, FALSE);
curl_setopt($crl, CURLOPT_SSL_VERIFYHOST, 2);
curl_setopt($crl, CURLOPT_URL, $url);
curl_setopt($crl, CURLOPT_HEADER, 0);
curl_setopt($crl, CURLOPT_RETURNTRANSFER, 1);
curl_setopt($crl, CURLOPT_POST, 1);
curl_setopt($crl, CURLOPT_POSTFIELDS, $data);
$response = curl_exec($crl);
curl_close($crl);
//echo $response;          
//ENd SMS API Code here your code

 } elseif($method == 'guest') {
//code to handle if customer is guest
 } else {				 
//code to handle for logged in customer
 }  
//END New Customer Registration SMS Here  


