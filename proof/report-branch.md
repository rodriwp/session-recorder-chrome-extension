# Session Report: Cross-site checkout

- **App:** http://localhost:5319
- **Date:** 2026-11-22T14:30:41.175Z
- **Duration:** 00:02
- **Verbosity level:** L0
- **Events:** 14

### Tabs

| Tab | Role | URL | Title |
| --- | --- | --- | --- |
| 463237461 | primary | http://localhost:5319/cross-site/index.html | Cross-site checkout |

## Timeline

⚠ **ERROR [00:00]** (log) Failed to load resource: the server responded with a status of 404 (File not found)

[00:00] 📷 Session start
![Session start](screenshots/001-0000.jpg)
[00:00] CLICK "Pay $120.00" (#pay, tab 463237461)

⚠ **ERROR [00:00]** (log) Failed to load resource: the server responded with a status of 404 (File not found)

[00:00] console.error @ http://pay.example.test:5319/cross-site/pay.html:20 · in cross-site iframe pay.example.test:5319
```
Payment declined: charge returned 501
```

⚠ **ERROR [00:00]** (exception) · in cross-site iframe pay.example.test:5319 Error: Charge failed with HTTP 501
```
    at <anonymous> (http://pay.example.test:5319/cross-site/pay.html:22:10)
```

⚠ **ERROR [00:00]** (log) · in cross-site iframe pay.example.test:5319 Failed to load resource: the server responded with a status of 501 (Unsupported method ('POST'))

[00:00] CLICK "Search orders" (#search, tab 463237461)

⚠ **ERROR [00:00]** (exception) · in worker localhost:5319/cross-site/search-worker.js Error: Search index unavailable (HTTP 404)
```
    at self.onmessage (http://localhost:5319/cross-site/search-worker.js:5:8)
```

[00:01] 🌐 404 GET /api/cart
- Response (text/html):
```html
<!DOCTYPE HTML>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <style type="text/css">
            :root {
                color-scheme: light dark;
            }
        </style>
        <title>Error response</title>
    </head>
    <body>
        <h1>Error response</h1>
        <p>Error code: 404</p>
        <p>Message: File not found.</p>
        <p>Error code explanation: 404 - Nothing matches the given URI.</p>
    </body>
</html>

```

[00:01] 🌐 501 POST /api/charge · in cross-site iframe pay.example.test:5319
- Request: _(not captured from a cross-site frame)_
- Response: _(not captured from a cross-site frame)_

[00:01] 🌐 404 GET /api/search?q=weekender · in worker localhost:5319/cross-site/search-worker.js
- Response (text/html):
```html
<!DOCTYPE HTML>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <style type="text/css">
            :root {
                color-scheme: light dark;
            }
        </style>
        <title>Error response</title>
    </head>
    <body>
        <h1>Error response</h1>
        <p>Error code: 404</p>
        <p>Message: File not found.</p>
        <p>Error code explanation: 404 - Nothing matches the given URI.</p>
    </body>
</html>

```

[00:01] HOVER button "Search orders" (#search, tab 463237461) for 0.7s
[00:01] 📷 screenshot (interaction)
![screenshot (interaction)](screenshots/002-0001.jpg)

## Appendix: Network Index

- [00:01] 404 GET http://localhost:5319/api/cart
- [00:01] 501 POST http://pay.example.test:5319/api/charge · in cross-site iframe pay.example.test:5319
- [00:01] 404 GET http://localhost:5319/api/search?q=weekender · in worker localhost:5319/cross-site/search-worker.js

## Appendix: Console Dump

```
[00:00] ERROR (log) Failed to load resource: the server responded with a status of 404 (File not found)
[00:00] ERROR (log) Failed to load resource: the server responded with a status of 404 (File not found)
[00:00] error · in cross-site iframe pay.example.test:5319: Payment declined: charge returned 501
[00:00] ERROR (exception) · in cross-site iframe pay.example.test:5319 Error: Charge failed with HTTP 501
[00:00] ERROR (log) · in cross-site iframe pay.example.test:5319 Failed to load resource: the server responded with a status of 501 (Unsupported method ('POST'))
[00:00] ERROR (exception) · in worker localhost:5319/cross-site/search-worker.js Error: Search index unavailable (HTTP 404)
```
