# Building a Raw Bitcoin Transaction in JavaScript

The updated code for the first chapter of the book : [Blockchain by Example](https://subscription.packtpub.com/book/big_data_and_business_intelligence/9781788475686).
This script creates an ```op_return``` output using bitcoinJs-lib as presented in the book.

## Instructions : <br>
1. Ensure you have [Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) installed
2. run ```npm install bitcoinjs-lib request request-promise```
4. Send some bitcoins from a [faucet website](https://testnet.manu.backend.hamburg/faucet) to ```n3CKupfRCJ6Bnmr78mw9eyeszUSkfyHcPy```
5. run ```node hello.js``` <br><br>
![](https://preview.ibb.co/jckrkp/nodejshello.png)

## P2SH or P2PKH : <br>
You can use the [blockcypher API](https://www.blockcypher.com/dev/bitcoin/#transaction-api) to determine whether the transaction output is a P2SH or P2PKH. Here is an [example]( https://api.blockcypher.com/v1/btc/test3/txs/0791521362528725683caedf998006cf68b1cd817be1694ef0daca265d9b4252?limit=50&includeHex=true) using our particular output.
```
"outputs": [
    {
      "value": 1253185750,
      "script": "76a914b9172e192d2805ea52fa975847eea0657e38fef888ac",
      "spent_by": "7f3773696c100f75637f2130713ed5b4e5a747f00fb2250e0334a89bafaa5284",
      "addresses": [
        "mxPd583YeW6iw3cCgfrmrdcXKG6PLM2fBj"
      ],
      "script_type": "pay-to-pubkey-hash"
    },
    {
      "value": 110000000,
      "script": "76a914edcce89f510bf95606ec6a79cb28a745c039e22088ac",
      "spent_by": "d3e300c2f2eedf673ab544f4c2b09063353e618ab8a0c9444e931d0145e43ded",
      "addresses": [
        "n3CKupfRCJ6Bnmr78mw9eyeszUSkfyHcPy"
      ],
      "script_type": "pay-to-pubkey-hash"
    }
  ]
```
