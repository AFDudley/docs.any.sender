# API

The REST API has two endpoints: /relay and /balance.

## Relay

The relay endpoint expects a POST with application/json body. The body is a [relay transaction](./relayTransaction.md).

The response is a relay transaction, signature from the receipt signer authority and the relay transaction id (the digest that was signed)

## Balance

The balance endpoint expects the address as it's single path parameter: `/balance/<address>`. It returns the balance of the address in the form:
```json
{
    "balance": "<balance>"
}
```