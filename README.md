# Rest API
Trade AI

## Generic API information

  
**Endpoint** : *https://exchange.populous.word/api/*

**Response header codes :**

  

- 200 = Success

- 400 = Bad requested data

- 401 = Unauthorized request

- 429 = API Limit exceeds

- 418 = IP Banned

  

**Response :**

  

- status = OK, NOT_OK

- message = Message related to response

- data = Additional data

  

## Authorization

  

### Headers

-  `api_key` : `YOUR_API_KEY`

-  `secret_key` : `YOUR_SECRET_KEY`(If required)

-  `Content-Type` : `application/x-www-form-urlencoded`

`API-keys and secret-keys`  **are case sensitive**.


## API Types

|API type | Description |
|--|--|
| TRADE |  Required API_KEY & SECRET_KEY  |
| USER_DATA | Not Available  |
| USER_STREAM | Not Available  |
| MARKET_DATA | Not Available  |


## Trade Types

|Trade type | Description |
|--|--|
| LIMIT | Buy/Sell with limit |
| MARKET_LIMIT | Buy/Sell with market limit |
| STOP_LIMIT | Buy/Sell with stop limit |

## TRADE : SIGNED Endpoint Examples for POST /api/order

|Key| Value |
|--|--|
| api_key | 7b091d38af495a67f50ef5c00c18d6ed0f0510a4aaffef6be38bd74cacf9db1c |
| secret_key | 1f1165313767f8f98d2f9c94a356303fe25ebc580cfb818fff63415232b5eeb7 |

-----

Parameter | Value
------------ | ------------
symbol | PPT_BTC
side | BUY
type | LIMIT
qty | 1
price | 0.1


* **curl command:**
```
curl -X POST \
  https://exchange.populous.word/api/order \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -H 'Postman-Token: 62822c3a-922e-47b2-9ffd-9c17a84dc872' \
  -H 'api_key: 7b091d38af495a67f50ef5c00c18d6ed0f0510a4aaffef6be38bd74cacf9db1c' \
  -H 'cache-control: no-cache' \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -H 'secret_key: 1f1165313767f8f98d2f9c94a356303fe25ebc580cfb818fff63415232b5eeb7' \
  -F symbol=DASH_USD \
  -F side=SELL \
  -F type=LIMIT \
  -F qty=1 \
  -F price=0.1
```
