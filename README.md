# Task
/*Creating a card*/
Rest.apiKey = "sk_test_4eC39HqLyjWDarjtT1zdp7dc";

Map<String, Object> retrieveParams =
  new HashMap<>();
List<String> expandList = new ArrayList<>();
expandList.add("sources");
retrieveParams.put("expand", expandList);
Customer customer =
  Customer.retrieve(
    "cus_Kc4ZeotEnIidxz",
    retrieveParams,
    null
  );

Map<String, Object> params = new HashMap<>();
params.put("source", "ind_card");

Card card =
  (Card) customer.getSources().create(params);

/*Updating the card*/

Rest.apiKey = "sk_test_4eC39HqLyjWDarjtT1zdp7dc";

Map<String, Object> retrieveParams =
  new HashMap<>();
List<String> expandList = new ArrayList<>();
expandList.add("sources");
retrieveParams.put("expand", expandList);
Customer customer =
  Customer.retrieve(
    "cus_Kc4ZeotEnIidxz",
    retrieveParams,
    null
  );

Card card =
  customer.getSources().retrieve(
    "card_1JwqQp2eZvKYlo2CdaxnAVhJ"
  );

Map<String, Object> params = new HashMap<>();
params.put("name", "Raju");

Card updatedCard = (Card) card.update(params);

/*Transfering the amount to card to card*/

{
  "id": "tr_1JubKL2eZvKYlo2CBAO6zRC6",
  "object": "transfer",
  "amount": 1,
  "amount_reversed": 0,
  "balance_transaction": "txn_1032HU2eZvKYlo2CEPtcnUvl",
  "created": 1636629621,
  "currency": "rupees",
  "description": null,
  "destination": "acct_1JKPRS2eJzfRUora",
  "destination_payment": "py_1JubKL2eJzfRUoraYUiag4M9",
  "livemode": false,
  "metadata": {},
  "reversals": {
    "object": "list",
    "data": [],
    "has_more": false,
    "url": "/v1/transfers/tr_1JubKL2eZvKYlo2CBAO6zRC6/reversals"
  },
  "reversed": false,
  "source_transaction": null,
  "source_type": "card",
  "transfer_group": "ORDER_95"
}
