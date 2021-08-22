# W.A.P.S

Application to display shipping quotes of an ecommerce. 🚛

# API endpoints

## AUTH

`POST` /login

Lets the user login into the system and generates a json web token for accessing the protected routes

## USER

`POST` /users

Register a new user and associates a saving fund by default

`GET` /users/balance

- Bearer token required

Lets an user list each fund with it's balance and the user total balance (BTC)

## FUNDS

`POST` /funds

- Bearer token required

Lets an user create a new checking fund

`PUT` /funds

- Bearer token required

Lets an user update the following fund fields:
  - Name
  - Description
  - Minimum Balance

`POST` /funds/transactions

- Bearer token required

Lets check all the selected fund transactions

`POST` /funds/internal-transfer

- Bearer token required

Lets an user transfer BTC between his funds

`POST` /funds/external-incoming

- Bearer token required

Lets an user transfer BTC from any wallet to one of his associated funds (incoming transactions)

`POST` /funds/external-outgoing

- Bearer token required

Lets an user transfer BTC from one of his funds to any wallet (outgoing transactions)

`GET` /funds/interest-rate

- Bearer token required

Lets an user check the estimated gain according to the plan associated to his saving fund and its current balance

## ADMIN

`POST` /funds/interest-earned

- Bearer token required and admin only

Lets the admin user transfer to each user's saving fund their gained monthly interests respectively






