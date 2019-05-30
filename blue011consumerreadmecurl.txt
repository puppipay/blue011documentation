A) Consuming by creating a JSON message in curl

A-1) Obtain API Key

A-1.1) Create consumer product

 You need to enter the blockchain address to receive funds in this product.
 This product will be useful to receive funds from messages

A-2) Create a JSON message as below

{"message":"eyJjcmMiOiJkMjJlN2YiLCJ1aWQiOiIwMjI3YTNhZDlmMWFmZjRlODcyNmQ3OTZkYTQ0YTFmNjJiYWM0Mjg3NDRhNjY5N2E5MTYzMzAxMzM4MTA4ZGEwYTgiLCJwaW5kYXRhIjp7ImlkIjoiVEVTMTU1NTc1Nzg5NTE2NiIsImRhdGUiOiIxNTU2MjczMTc5OTI0IiwicGluIjoiIn19","pin":"PIN_OOEFW8G5R","target":"8uk4xeCwtjGpQ6TBPx5vrQwXVkjCi9ZZ18"}

A-2.1) Field details 

message:''  
pin:''  
target:'' //optional

If not set, the asset goes to address set in creation of account.


A-3) Consume message as below

curl -X POST -H "Content-Type: application/json" -H "Authorization: ApiKey eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjYmFmZjg5OTFjYzkyNWQwNWI3YjI3NCIsImlhdCI6MTU1NTc1OTI4NiwiZXhwIjoxNTYzNTM1Mjg2fQ.21-x_rAJHfoMcPZHWajeow7jXW-y7CZif6SfutCgYWk" \
 -d @blue011consumemessage3.json \
 https://dashrevert.belavaditech.com/consumemessage


A-4) Output looks like below

{
  "amount": 343994,
  "address": "8uk4xeCwtjGpQ6TBPx5vrQwXVkjCi9ZZ18",
  "txid": "7ad6815581ada835abbba56ab433029380bba870cde73c2dbc8ec35589f43c94"
}

A-5) Error detection 

Invalid address
Invalid message
Invalid pin
Invalid API-key
No balance     

B) Consuming by creating a text message in curl

B-1) Obtain API Key

B-1.1) Create consumer product

 You need to enter the blockchain address to receive funds in this product.
 This product will be useful to receive funds from messages

B-2) Create a text message as below

message=eyJjcmMiOiJkMjJlN2YiLCJ1aWQiOiIwMjI3YTNhZDlmMWFmZjRlODcyNmQ3OTZkYTQ0YTFmNjJiYWM0Mjg3NDRhNjY5N2E5MTYzMzAxMzM4MTA4ZGEwYTgiLCJwaW5kYXRhIjp7ImlkIjoiVEVTMTU1NTc1Nzg5NTE2NiIsImRhdGUiOiIxNTU2MjczMTc5OTI0IiwicGluIjoiIn19&&pin=PIN_OOEFW8G5R&&target=8uk4xeCwtjGpQ6TBPx5vrQwXVkjCi9ZZ18

B-3) Consume message as below
curl -X POST -H "Authorization: ApiKey eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjYmFmZjg5OTFjYzkyNWQwNWI3YjI3NCIsImlhdCI6MTU1NTc1OTI4NiwiZXhwIjoxNTYzNTM1Mjg2fQ.21-x_rAJHfoMcPZHWajeow7jXW-y7CZif6SfutCgYWk" \
 -d @blue011consumemessage2.txt \
 https://dashrevert.belavaditech.com/consumemessage

B-4) Output

{
  "amount": 6880,
  "address": "8uk4xeCwtjGpQ6TBPx5vrQwXVkjCi9ZZ18",
  "txid": "eb9146ec359101def6fd3504f0a2e0276eb9dc76cbbfa5acab067599dd58a9bf"
}

B-5) Error detection

Invalid address
Invalid message
Invalid pin
Invalid API-key
No balance

