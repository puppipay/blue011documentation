Issuing message in a Ionic4 mobile/web app


1) Obtain API key 

1.1) Create issuer product

 You need to enter the blockchain address to receive funds in this product.
 This product will be useful to send funds as messages


2) Create document mentioning type of message to issue

Create a JSON message as below

details = {"msgtype":"default", "network":"testnet"}


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


 url = "https://dashrevert.belavaditech.com"
 apikey = "ApiKey eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjYmFmZjg5OTFjYzkyNWQwNWI3YjI3NCIsImlhdCI6MTU1NTc1OTI4NiwiZXhwIjoxNTYzNTM1Mjg2fQ.21-x_rAJHfoMcPZHWajeow7jXW-y7CZif6SfutCgYWk";


issuemessage (details: any) {


        return new Promise((resolve, reject) => {


             let headers = new Headers();
             headers.append('Authorization', apikey);
             headers.append('Content-Type', 'application/json');

            this.http.post(url + '/issuemessage', JSON.stringify(details), {headers: headers})
              .subscribe(res => {

                let data = res.json();
                resolve(data);

              }, (err) => {
                reject(err);
              });

        });



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
