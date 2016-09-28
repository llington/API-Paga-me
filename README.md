curl -X POST 'https://api.pagar.me/1/transactions' \
-d 'api_key=ak_test_grXijQ4GicOa2BLGZrDRTR5qNQxJW0' \
-d 'amount=1000' \
-d 'card_hash={CARD_HASH}' \
-d 'postback_url=http://seusite.com/payments/2718' \
-d 'split_rules[0][recipient_id]=re_ci7nhf1ay0007n016wd5t22nl'
-d 'split_rules[0][charge_processing_fee]=true' \
-d 'split_rules[0][liable]=true' \
-d 'split_rules[0][percentage]=30' \
-d 'split_rules[1][recipient_id]=re_ci7nheu0m0006n016o5sglg9t' \
-d 'split_rules[1][charge_processing_fee]=true' \
-d 'split_rules[1][liable]=false' \
-d 'split_rules[1][percentage]=70'
{
"object": "transaction",
"status": "processing",
"refuse_reason": null,
"status_reason": "acquirer",
"acquirer_response_code": null,
"authorization_code": null,
"soft_descriptor": "API-paga-me",
"tid": null,
"nsu": null,
"date_created": "2015-02-25T21:54:56.000Z",
"date_updated": "2015-02-25T21:54:56.000Z",
"amount": 310000,
"installments": 5,
"id": 184220,
"cost": 0,
"postback_url": "http://requestb.in/pkt7pgpk",
"payment_method": "credit_card",
"antifraud_score": null,
"boleto_url": null,
"boleto_barcode": null,
"boleto_expiration_date": null,
"referer": "api_key",
"ip": "189.8.94.42",
"subscription_id": null,
"phone": null,
"address": null,
"customer": null,
"card": {
"object": "card",
"id": "card_ci6l9fx8f0042rt16rtb477gj",
"date_created": "2015-02-25T21:54:56.000Z",
"date_updated": "2015-02-25T21:54:56.000Z",
"brand": "mastercard",
"holder_name": "Api Customer",
"first_digits": "548045",
"last_digits": "3123",
"fingerprint": "HSiLJan2nqwn",
"valid": null
},
"metadata": {
"idccount": "58054"
}
}

curl -X POST https://api.pagar.me/1/recipients \
-d 'api_key=ak_test_grXijQ4GicOa2BLGZrDRTR5qNQxJW0' \
-d 'transfer_interval=weekly' \
-d 'transfer_day=5' \
-d 'transfer_enabled=true' \
-d 'bank_account_id=4841'
{
"object": "recipient",
"id": "re_ci9bucss300h1zt6dvywufeqc",
"bank_account": {
"object": "bank_account",
"id": 4841,
"bank_code": "341",
"agencia": "0932",
"agencia_dv": "5",
"conta": "58054",
"conta_dv": "1",
"document_type": "cpf",
"document_number": "26268738888",
"legal_name": "API BANK ACCOUNT",
"charge_transfer_fees": false,
"date_created": "2016-08-19T15:40:51.000Z"
},
"transfer_enabled": true,
"last_transfer": null,
"transfer_interval": "weekly",
"transfer_day": 5,
"automatic_anticipation_enabled": true,
"anticipatable_volume_percentage": 85,
"date_created": "2015-05-05T21:59:48.000Z",
"date_updated": "2015-05-06T22:51:48.000Z"
}

curl -X POST https://api.pagar.me/2/recipients \
-d 'api_key=ak_test_grXijQ4GicOa2BLGZrDRTR5qNQxJW1' \
-d 'transfer_interval=weekly' \
-d 'transfer_day=12' \
-d 'transfer_enabled=true' \
-d 'bank_account_id=4855'
{
"object": "recipient",
"id": "re_ci9bucss300h1zt6dvywufeqc",
"bank_account": {
"object": "bank_account",
"id": 4855,
"bank_code": "341",
"agencia": "0932",
"agencia_dv": "5",
"conta": "58054",
"conta_dv": "1",
"document_type": "cpf",
"document_number": "26268738888",
"legal_name": "API BANK ACCOUNT",
"charge_transfer_fees": false,
"date_created": "2016-03-21T12:40:51.000Z"
},
"transfer_enabled": true,
"last_transfer": null,
"transfer_interval": "weekly",
"transfer_day": 12,
"automatic_anticipation_enabled": true,
"anticipatable_volume_percentage": 85,
"date_created": "2016-03-21T20:43:48.000Z",
"date_updated": "2016-03-21T21:50:48.000Z"
}
[{
"object": "payable",
"id": 1485,
"status": "paid",
"amount": 39000,
"fee": 115,
"installment": null,
"transaction_id": 192669,
"split_rule_id": "sr_ci87hce8o00083016bkniqems",
"payment_date": "2015-04-07T03:00:00.000Z",
"type": "credit",
"payment_method": "boleto",
"date_created": "2015-04-07T15:47:48.000Z"
}, 

{
"object": "payable",
"id": 1486,
"status": "paid",
"amount": 91000,
"fee": 0,
"installment": null,
"transaction_id": 192669,
"split_rule_id": "sr_ci87hce8o00093016fin8p6ll",
"payment_date": "2015-04-07T03:00:00.000Z",
"type": "credit",
"payment_method": "boleto",
"date_created": "2015-04-07T15:47:48.000Z"
}]


