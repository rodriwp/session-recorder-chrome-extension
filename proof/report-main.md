# Session Report: Cross-site checkout

- **App:** http://localhost:5319
- **Date:** 2026-11-22T14:17:54.131Z
- **Duration:** 00:02
- **Verbosity level:** L0
- **Events:** 9

### Tabs

| Tab | Role | URL | Title |
| --- | --- | --- | --- |
| 2074914626 | primary | http://localhost:5319/cross-site/index.html | Cross-site checkout |

## Timeline

⚠ **ERROR [00:00]** (log) Failed to load resource: the server responded with a status of 404 (File not found)

[00:00] 📷 Session start
![Session start](screenshots/001-0000.jpg)
[00:00] CLICK "Pay $120.00" (#pay, tab 2074914626)

⚠ **ERROR [00:00]** (log) Failed to load resource: the server responded with a status of 404 (File not found)

[00:00] CLICK "Search orders" (#search, tab 2074914626)

⚠ **ERROR [00:00]** (log) Uncaught (in promise) Error: Search index unavailable (HTTP 404)
```
    at self.onmessage (http://localhost:5319/cross-site/search-worker.js:5:8)
```

[00:00] 🌐 404 GET /api/cart
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

[00:01] 📷 screenshot (interaction)
![screenshot (interaction)](screenshots/002-0001.jpg)
[00:01] HOVER button "Search orders" (#search, tab 2074914626) for 0.7s

## Appendix: Network Index

- [00:00] 404 GET http://localhost:5319/api/cart

## Appendix: Console Dump

```
[00:00] ERROR (log) Failed to load resource: the server responded with a status of 404 (File not found)
[00:00] ERROR (log) Failed to load resource: the server responded with a status of 404 (File not found)
[00:00] ERROR (log) Uncaught (in promise) Error: Search index unavailable (HTTP 404)
```
