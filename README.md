# Amwaly_Objective-c
Use this Amwaly Objective c payment gateway to enable clients of your App to pay using Amwaly gateway.


## Usage

If you're using AmwalyCreateUrlPayment, you can call import it into your App.

```objective-c
#import "AmwalyCreateUrlPayment.h"

```


Make sure you've set up the macros in AmwalyCreateUrlPayment.m beforehand.



```objective-c
NSString *Amwaly_Url   = @"";
NSString *Amwaly_Key   = @"";
NSString *Amwaly_Email = @"";
```

Calling it is even easier.

How To Use V1 WithOut Client Deatils


```objective-c
NSString *Amwaly_Product              = @"Order 10#"; // Name Product
NSString *Amwaly_Total                = @"10"; // Amount USD 
NSString *Amwaly_callback_url         = @"https://yourdomen.com/Amwaly/callback"; // After Payment Completed will back the your url


NSString * PaymentUrl = [AmwalyCreateUrlPayment 
CreatePaymentUrlWithOutClientDeatils:Amwaly_Product
Total:Amwaly_Total
callback_url:Amwaly_callback_url
];

NSLog(@"Payment Url is : %@",PaymentUrl);

```


How To Use V2 With Client Deatils


```objective-c
NSString *Amwaly_Product              = @"Order 10#"; // Name Product
NSString *Amwaly_amount               = @"10"; // Amount USD 
NSString *Amwaly_callback_url         = @"https://yourdomen.com/Amwaly/callback"; // After Payment Completed will back the your url
NSString *Amwaly_customer_email       = @"email@email.com"; // Email Customer
NSString *Amwaly_billing_street1      = @"Dubae"; // Billing Street 1
NSString *Amwaly_billing_city         = @"Dubae"; // Customer City
NSString *Amwaly_billing_state        = @"Dubae Street "; // Billing State
NSString *Amwaly_billing_country      = @"AE";// Customer Country  like AE - IQ - FR etc...
NSString *Amwaly_billing_postcode     = @"10013"; // Customer ZIP Code
NSString *Amwaly_customer_givenName   = @"Azozz"; // Customer First Name
NSString *Amwaly_customer_surname     = @"ALFiras"; // Customer Last Name
NSString *Amwaly_customer_phonenumber = @"9647719675127"; // Customer Phone Number


NSString * PaymentUrl = [AmwalyCreateUrlPayment 
CreatePaymentLink:Amwaly_Product
amount:Amwaly_amount
callback_url:Amwaly_callback_url
customer_email:Amwaly_customer_email
billing_street1:Amwaly_billing_street1
billing_city:Amwaly_billing_city
billing_state:Amwaly_billing_state
billing_country:Amwaly_billing_country
billing_postcode:Amwaly_billing_postcode
customer_givenName:Amwaly_customer_givenName
customer_surname:Amwaly_customer_surname
customer_phonenumber:Amwaly_customer_phonenumber
];

NSLog(@"Payment Url is : %@",PaymentUrl);

```
