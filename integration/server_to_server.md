# Server-to-Server Integration Guide

## Step 1: Get the Task Feed

Request:

```
https://wallapi.tappads.io/v1/feed?apikey={API_KEY}&user_id={TELEGRAM_USER_ID}&ip={IP}&ua={USER_AGENT}&lang={LANG}&is_premium={IS_PREMIUM}
```

Response:

```json
[
  {
    "id": 5,
    "name": "Spin the reels",
    "icon": "https://site.com/icon.jpg",
    "url": "https://t.me/the_bot?start=123",
    "payout": 0.04,
    "currency": "USDT",
    "is_done": false
  }
]
```

## Step 2: Handle Clicks

Send a `GET` request to the `click_postback` URL included in the feed.

## Step 3: Check Task Completion

Use:

```
https://wallapi.tappads.io/v1/check-complete?apikey={API_KEY}&offer_id={OFFER_ID}&telegram_id={TELEGRAM_ID}
```

Response:

```json
{ "complete": true }
```