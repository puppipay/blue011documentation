
# Message contract based Blockchain Payment Solution (BLUE011)

A message contract based payment solution using DASH blockchain. It can be used by calling a REST-api.

It can be used with loyalty coupons, where the **COUPONS** can be issued with money present in coupon protected by a **PIN** . The receiver of coupon can accept payment in his wallet by providing the **PIN**.

Settlement happens in DASH blockchain in about 6 minutes.

Other usecases
- Revertible payments on blockchain.
- Point of Sale terminals can issue coupons.
- Mobile wallets can send payments as message.
- ATMs can issue coupons if they don't have cash.
- Name etching on blockchain.

## Background
- Writing smart contract using Bitcoin, Dash type blockchain difficult
- Ethereum and Hyperledger needs more infrastructure
- Stellar and Ripple similar to Bitcoin type, with additional features

The above was not easily usable in ATMs and Asynchronous payment mechanisms.

To solve above issues, this technology is invented.

## Benefits

To compare other payment mechanisms with above method
- Using standard Bitcoin, Dash, Litecoin, Bitcoincash the transfer has to be done directly to receivers blockchain-address.
- Above cannot be used to send crypto as message, it cannot be used in ATM, it cannot be used in email.
- Using ethereum, it requires more maintenance of smart-contract
- Using stellar, ripple limitation is similar to bitcoin.
- Using hyperledger we are not sure.

Using the provided technology, crypto-coins can be sent as messages in whatsapp, can be used in ATMs, can be used in loyalty coupons, with minimum expenses and minimum infrastructure.

# Documentation

## Getting started

Below document explains how to get started.

- [Getting started ](blue011gettingstarted.txt)

## Examples

Below document explains curl examples to Issue and Consume payment messages

### Curl examples

- [Issuing payment messages ](blue011issuerreadmecurl.txt)
- [Consuming payment messages  ](blue011consumerreadmecurl.txt )

Below document explains Ionic4 javascript examples to Issue and Consume payment messages
### Ionic4 javascript examples

- [Issuing payment messages ](blue011issuerreadmeionic4.txt)
- [Consuming payment messages  ](blue011consumerreadmeionic4.txt )


## References

Below document gives information on testnet and livenet links to broadcast transaction.

It has links to create testnet and livenet DASH wallet. 

- [Resources ](blue011resources.txt)

## Issuing charges

Cost of using the services

- Developer is charged 2 tokens per successful request( 10 cents approx), 

- Developer can buy tokens - 100$ for 2000 tokens.

- 2000 tokens are given free on creating account for evaluation.

## Consuming charges

- A charge of min 1% is collected from user transaction.

- Developer is charged 1 token per wrong request( 5  cents approx), 

- Developer is not charged for correct request  

## User charges

The charges the user of solution will incur.

- Users pays for developer income, service charges

- Developer income is collected from user per transaction and credited to developers blockchain address

- Our fees is collected from user per transaction and credited to our blockchain address

Typically 

Our fees = Developer fees.

(ie) User pays = twice developer fees + network fees.


## Income to developer

- Developer can charge fees to his clients

- It can be 0.1% to 3% fees per transaction. 

- The transaction can be sending, receiving, reverting.

- Developers income is collected from user per transaction and credited to developers DASH blockchain address

## Terms and Conditions

- The provided samples and libraries is for evaluation
- Different setup is provided for production environment
- All terms, prices subject to change.

## Evaluation setup    

- Available for testnet 
- Available for livenet

## Notes
1) These are one time use messages. It cannot be used and should not be used more than once, as data will be visible in public blockchain.

2) The PIN data will be visible in public after transaction is executed in BLUE011 product type.

3) The protection of PIN data will be available in other products like BLUE021.


