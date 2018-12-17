# Pre-Approved-Payments

Using this API merchants will be able to charge User from their Cofred Account

HTTP Method: POST

# Resource Url

https://cofredpayaccess.com/api/v1/ApprovePayment

# Headers

See our Guide for how to setup Header https://github.com/cofred/Header-Authentication

# Authentication Headers Example

merchant_id: VF9CMTY3WURPZUpJdkNnVWJWRXE=   // Base64 Encoded

secret_code: I8AtLUljNqcdS4F76OVy2Zf1bJvGwsP95rE

terminal_id: YINCU

access_token: dUp4dEtybVg0Ump4MEFT  // Base64 Encoded

timestamp: 1505628722 // Current Time in Unix Format

# Request Parameters

Field	M/O	Length	Format	Description

Account Number M	10 Numeric 	Account Number to which you want to send request

Currency Symbol M 3 Letters Currency Symbol of Debit Amount

Amount M .. Debit Amount

Order ID >6 Alpha Numeric Oder ID to identify transaction details to Merchant

# Sending Parameters

account_number (For Account Number)
currency_symbol (Account Symbol)
amount (Debit Amount)
order_id (Order ID for Merchant side Identification)

# API Response

A HTTP response code 200 is sent back for success

# Response Parameters

Field	Description

responseCode	Response Code

responseMessage Response Message

TransactionReference Account Number

order_id Order ID as sent in Input

symbol Currency Symbol

amount Debited Amount

TransactionDate Account Holder Name

# Sample Response

200

{
  "responseCode":"200",
  
  "responseMessage":"Pre-approval payment request was successful.",
  
  "TransactionReference":"67565545",
  
  "order_id":"NJHFHGH786", // Passed by merchant
  
  "symbol":"GHS",
  
  "amount":"50",
  
  "TransactionDate":"2018-12-01 09:10:00"
}

# Communication

Requests will be sent over the REST protocol using POST Method.
