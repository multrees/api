# Multrees WebAPI API documentation version 1
https://api.multrees.com/v{version}/{fi}

---

## Clients
Collection of all clients

### /clients

* **get**: Retrieve all clients.
* **post**: Create a number of new clients - TBD.
* **put**: Update a number of existing clients - TBD.
* **delete**: Remove a number of clients - TBD.

### /clients/{client}
An individual or organisation investor

* **get**: Retrieve client details.
* **post**: Create a new client - TBD.
* **put**: Update an existing client - TBD.
* **delete**: Remove a client - TBD.

## Accounts
Collection of all investment and cash accounts

### /accounts

* **get**: Retrieve all cash and investment accounts.
* **post**: Create a number of new accounts - TBD.
* **put**: Update a number of existing accounts - TBD.
* **delete**: Remove a number of accounts - TBD.

### /accounts/{account}
Investment or cash accounts

* **get**: Retrieve an account.
* **post**: Create a new account - TBD.
* **put**: Update an existing account - TBD.
* **delete**: Remove an account - TBD.

## Reporting Groups
Collection of groups of accounts for reporting

### /reportinggroups

* **get**: Retrieve all reporting groups
* **post**: Create a number of new reporting groups - TBD.
* **put**: Update a number of existing reporting groups - TBD.
* **delete**: Remove a number of reporting groups - TBD.

### /reportinggroups/{ReportingGroup}
Groups of accounts for reporting

* **get**: Retrieve a reporting group.
* **post**: Create a new reporting group - TBD.
* **put**: Update an existing reporting group - TBD.
* **delete**: Remove an reporting group - TBD.

## Beneficiaries
Collection of all beneficiaries for a client

### /beneficiaries

* **get**: Retrieve all beneficiaries.
* **post**: Create a number of new beneficiaries - TBD.
* **put**: Update a number of existing beneficiaries - TBD.
* **delete**: Remove a number of beneficiaries - TBD.

### /beneficiaries/{beneficiary}
A beneficiary of the client

* **get**: Retrieve a beneficiary.
* **post**: Create a new beneficiary - TBD.
* **put**: Update an existing beneficiary - TBD.
* **delete**: Remove a beneficiary - TBD.

## Holdings
Collection of all holdings for a client.

### /holdings

* **get**: Retrieve all holdings.

### /holdings/{holding}
A specific holding in an asset

* **get**: Retrieve specific holdings.

### /holdings/{holding}/classifications/{classification}

* **get**: 

### /holdings/{holding}/accounts/{account}

* **get**: 

## Payments
Collection of all payments made for an account or client.

### /payments

* **get**: Retrieve all payments.
* **post**: Create a number of payments - TBD.

### /payments/{payment}
A single payment from an account.

* **get**: Retrieve a payment.
* **post**: Create a payment - TBD.

## FXs
Collection of all FXs made for an account or client.

### /FXs

* **get**: Retrieve all FXs.
* **post**: Create a number of FXs - TBD.

### /FXs/{FX}
A single FX from an account.

* **get**: Retrieve a FX.
* **post**: Create a FX - TBD.

## Trades
Collection of all trades.

### /trades

* **get**: Retrieve all trades.

### /trades/{trade}
A single trade on an account

* **get**: Retrieve a single trade.

## Corporate Actions Notifications/Elections
Collection of all corporate actions

### /corporateactions

* **get**: Retrieve all corporate actions notifications - TBD.
* **put**: Elect on a number of corporate actions - TBD.

## Users
Collection of all users of the Multrees Web API.

### /users

* **get**: Retrieve all users.

### /users/{user}
A user of the Multrees Web API

* **get**: Retieve a user.

