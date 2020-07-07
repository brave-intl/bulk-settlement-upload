# uphold bulk settlement api

get the payouts associated with a particular card

```
GET https://api-sandbox.uphold.com/v0/me/cards/{card}/payouts
```

create a payout by sending transactions
```
POST https://api-sandbox.uphold.com/v0/me/cards/{card}/payouts
  [{
    ContactId: '?',
    denomination: {
      amount: '1.000000000000000000',
      currency: 'BAT'
    },
    destination: 'payout-address-uuid',
    origin: '? why if going through card',
    message: '',
    priority: 'normal/fast',
    reference: '?'
  }]
```

get status info about a payout in aggregate
```
GET https://api-sandbox.uphold.com/v0/me/cards/{card}/payouts/{payout}
```

get info about transactions for a payout. presented using pagination.
```
GET https://api-sandbox.uphold.com/v0/me/cards/{card}/payouts/{payout}/transactions
```