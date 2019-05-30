Issuing message using curl


1) Obtain API key 

 1.1) Create issuer product

 You need to enter the blockchain address to receive funds in this product.
 This product will be useful to send funds as messages


2) Create document mentioning type of message to issue

blue011issuemessage1.txt 

msgtype=default

2.1) Other options will be available

A) Custom pin option (future)
msgtype=custompin
pin=ABD345

B) Custom uid option (future)
msgtype=customuid
uid=''

C) Custom json pin option (future)
msgtype=customjsonpin
pin='stringified json'      


3) Issue command as follows to get the message issued

curl -X POST -H "Authorization: ApiKey eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjYzE0N2ZjNzIwMWRkNDIxYWVjYzc0YyIsImlhdCI6MTU1NjE3MDc2MSwiZXhwIjoxNTYzOTQ2NzYxfQ.Hb9pgaixBJvHKztUqNTgtE8Czi2a8rc8_rAs9JZbJ8U" \
 -d @blue011issuemessage1.txt \
 https://dashrevert.belavaditech.com/issuemessage


4) Output will look like below

{
  "message": "eyJjcmMiOiJkYWZiYWYiLCJ1aWQiOiIwMzM1ZGZkYjJkOTcxNzRmOGExMWQ0MDVlY2ZiNTI0MTUzODE3YjkxMDM3MDhmMmU1NjA5MjQ5MjU2ODVjNjMxZjIiLCJwaW5kYXRhIjp7ImlkIjoiVEVTMTU1NTc1Nzg5NTE2NiIsImRhdGUiOiIxNTU3NDg0ODAwMDE4IiwicGluIjoiIn19",
  "pin": "PIN_MZ41RDPCH",
  "address": "8hsH14uJbM9hFnvQQHY4TELRpNgogAFcY4",
  "fullredeemurl": "",
  "partredeemurl": "",
  "shorturl": ""
}

5) Error detection 

Invalid API-key
