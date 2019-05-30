A) Consuming message in a Ionic4 mobile/web app

A-1) Obtain API Key

A-1.1) Create consumer product

 You need to enter the blockchain address to receive funds in this product.
 This product will be useful to receive funds from messages

A-2) Create a JSON message as below

details = {"message":"eyJjcmMiOiJkMjJlN2YiLCJ1aWQiOiIwMjI3YTNhZDlmMWFmZjRlODcyNmQ3OTZkYTQ0YTFmNjJiYWM0Mjg3NDRhNjY5N2E5MTYzMzAxMzM4MTA4ZGEwYTgiLCJwaW5kYXRhIjp7ImlkIjoiVEVTMTU1NTc1Nzg5NTE2NiIsImRhdGUiOiIxNTU2MjczMTc5OTI0IiwicGluIjoiIn19","pin":"PIN_OOEFW8G5R","target":"8uk4xeCwtjGpQ6TBPx5vrQwXVkjCi9ZZ18"}

A-2.1) Field details 

message:''  
pin:''  
target:'' //optional

If not set, the asset goes to address set in creation of account.


A-3) Consume message as below


 url = "https://dashrevert.belavaditech.com"
 apikey = "ApiKey eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjYmFmZjg5OTFjYzkyNWQwNWI3YjI3NCIsImlhdCI6MTU1NTc1OTI4NiwiZXhwIjoxNTYzNTM1Mjg2fQ.21-x_rAJHfoMcPZHWajeow7jXW-y7CZif6SfutCgYWk";

 consumemessage (details: any) {


        return new Promise((resolve, reject) => {


             let headers = new Headers();
             headers.append('Authorization', apikey);
             headers.append('Content-Type', 'application/json');

            this.http.post(url + '/consumemessage', JSON.stringify(details), {headers: headers})
              .subscribe(res => {

                let data = res.json();
                resolve(data);

              }, (err) => {
                reject(err);
              });

        });


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

