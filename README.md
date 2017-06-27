# Multrees WebAPI API documentation version 1
https://api.multrees.com/v{version}/{fi}

---

## Clients
Collection of all clients ... [TODO]

### /clients

* **get**: Retrieve all clients. queryParameters

### /clients/{client}
An individual or organisation investor

* **get**: Retrieve client details.

## Accounts
Collection of all investment and cash accounts

### /accounts

* **get**: Retrieve all cash and investment accounts. Group

### /accounts/{account}
Investment or cash accounts

* **get**: Retrieve an account.

## Beneficiaries
Collection of all beneficiaries for a client

### /beneficiaries

* **get**: Retrieve all beneficiaries. queryParameters

### /beneficiaries/{beneficiary}
A beneficiary of the client

* **get**: Retrieve a beneficiary.

## Holdings
Collection of all holdings cor a client.

### /holdings

* **get**: Retrieve all holdings.

### /holdings/{holding}
A specific holding in an asset

* **get**: 

### /holdings/{holding}/classifications/{classification}

* **get**: 

### /holdings/{holding}/accounts/{account}

* **get**: 

## Payments
Collection of all payments made for an account or client.

### /payments

* **get**: Retrieve all payments.

### /payments/{payment}
A single payment from an account.

* **get**: Retrieve a payment.

## Trades
Collection of all trades.

### /trades

* **get**: Retrieve all trades.

### /trades/{trade}
A singel trade on an account

* **get**: Retrieve a single trade.

## Users
Collection of all users of the Multrees Web API.

### /users

* **get**: Retrieve all users.

### /users/{user}
A user of the Multrees Web API

* **get**: Retieve a user.

