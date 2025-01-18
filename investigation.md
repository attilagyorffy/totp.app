# investigation log

## What is `t999ru` referenced in `assets/index-gDJI-pzw.js`?

```shell
❯ curl -iL t999.ru
HTTP/1.1 301 Moved Permanently
Date: Sat, 18 Jan 2025 11:29:42 GMT
Content-Type: text/html
Content-Length: 167
Connection: keep-alive
Cache-Control: max-age=3600
Expires: Sat, 18 Jan 2025 12:29:42 GMT
Location: https://pdz.me/domain/t999.ru/
Report-To: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v4?s=POhJil3FYu1%2Fgth%2Fbav8%2FMtnlgXrum3bafjgg%2B8NiS3SKs1DZiVm8uRdRqaY7j2f99h3MgzfCbdy0cl3JPX%2BOuc85GmgesU2EV%2BNsrOfuIvyY98Kkzj4spRZ"}],"group":"cf-nel","max_age":604800}
NEL: {"success_fraction":0,"report_to":"cf-nel","max_age":604800}
Server: cloudflare
CF-RAY: 903e3fb2cb74324d-VIE

HTTP/2 404
date: Sat, 18 Jan 2025 11:29:43 GMT
content-type: text/html; charset=utf-8
access-control-allow-origin: *
cache-control: no-store
referrer-policy: strict-origin-when-cross-origin
x-content-type-options: nosniff
report-to: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v4?s=Qnl2esuBZo2633xrCvoVYGNDu%2FQV3YOvBvCuoG5AW37w07GiNl93k5vOMoG%2BV6iQtLYVo%2Fzr4fCe64xhNpAfl9EyJU6%2Fg7Fqs8tVj%2FAMSX2VjVVM5wQlPvM%3D"}],"group":"cf-nel","max_age":604800}
nel: {"success_fraction":0,"report_to":"cf-nel","max_age":604800}
vary: Accept-Encoding
cf-cache-status: DYNAMIC
server: cloudflare
cf-ray: 903e3fb54968e5a9-DFW
alt-svc: h3=":443"; ma=86400
server-timing: cfL4;desc="?proto=TCP&rtt=144883&min_rtt=144662&rtt_var=54691&sent=7&recv=8&lost=0&retrans=0&sent_bytes=2886&recv_bytes=535&delivery_rate=19667&cwnd=32&unsent_bytes=0&cid=663e8d78e615cd22&ts=201&x=0"

<html><head><meta http-equiv=Refresh content="0;url=/"></head><body><script>document.location='/';</script></body></html>⏎
```

## What is pdz.me?

```shell
❯ curl -iL 'https://pdz.me'
HTTP/2 103
link: <https://fonts.googleapis.com>; rel=preconnect

HTTP/2 200
date: Sat, 18 Jan 2025 11:30:15 GMT
content-type: text/html; charset=utf-8
access-control-allow-origin: *
cache-control: public, max-age=0, must-revalidate
link: <https://fonts.googleapis.com>; rel="preconnect"
referrer-policy: strict-origin-when-cross-origin
x-content-type-options: nosniff
report-to: {"endpoints":[{"url":"https:\/\/a.nel.cloudflare.com\/report\/v4?s=H03jZIvL7Tf%2FeSivFRiFHJNWDwkEORbxEGZla%2BCXTBgTYYa%2F2TfleJCHT%2F%2FDny9V%2BJ6MgoGJqGfxK1XXN7pzbTAUYFtG3KbuNSWoFHD5He0FkGiqEW0eolI%3D"}],"group":"cf-nel","max_age":604800}
nel: {"success_fraction":0,"report_to":"cf-nel","max_age":604800}
vary: Accept-Encoding
cf-cache-status: DYNAMIC
server: cloudflare
cf-ray: 903e407dbe2fe583-DFW
alt-svc: h3=":443"; ma=86400
server-timing: cfL4;desc="?proto=TCP&rtt=154797&min_rtt=154504&rtt_var=58526&sent=7&recv=8&lost=0&retrans=0&sent_bytes=2936&recv_bytes=522&delivery_rate=18360&cwnd=32&unsent_bytes=0&cid=40136e8840817ec6&ts=209&x=0"

<!DOCTYPE html><html lang="ru"><head><meta charset="utf-8"><meta http-equiv="X-UA-Compatible" content="IE=edge"><meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no"><link rel="preconnect" href="https://fonts.googleapis.com"><link rel="preconnect" href="https://fonts.gstatic.com" crossorigin><link href="https://fonts.googleapis.com/css2?family=Roboto+Condensed:wght@300;400;700&display=swap" rel="stylesheet"><link rel="icon" href="/favicon.ico"><title>PDZ.ME</title><link href="/css/app.c5a2b034.css" rel="stylesheet" crossorigin="anonymous" integrity="sha384-PjO0xvF9lzkNttlce2Y44oNRJAAeCKjOWIlSWvuqFIJ5///Q8ZFIRU73kHuUoY+S"></head><body><div id="app"></div><script src="/js/chunk-vendors.b12fc39a.js" crossorigin="anonymous" integrity="sha384-dMP139+JzKqTGlB3BHEXHfdV9gau+dbDO6puI6RCx3SLbNzVM8WjffnfzyIeLd90"></script><script src="/js/app.65b27f18.js" crossorigin="anonymous" integrity="sha384-0Wrod7Osv/fNmrXNbTaxXoXYp540HbkV01Mvh3YldO139Gk5zUayskohYYStcFhe"></script></body></html>⏎
```

## Where is counter.yadro.ru?

```shell
❯ nslookup counter.yadro.ru
Server:         8.8.8.8
Address:        8.8.8.8#53

Non-authoritative answer:
Name:   counter.yadro.ru
Address: 88.212.202.52
Name:   counter.yadro.ru
Address: 88.212.201.204
Name:   counter.yadro.ru
Address: 88.212.201.198
```


## What does the tracking code do?


```javascript
X0 = (e = "t999ru", t) => {
  try {
    const n = new URL(document.URL);
    typeof t == "function" && t(n);
    const s = e,
      i =
        "//counter.yadro.ru/hit" +
        (s ? ";" + s : "") +
        "?t" +
        "45.6" +
        ";r" +
        encodeURIComponent(document.referrer) +
        (typeof screen > "u"
          ? ""
          : ";s" +
            screen.width +
            "*" +
            screen.height +
            "*" +
            (screen.colorDepth ? screen.colorDepth : screen.pixelDepth)) +
        ";u" +
        encodeURIComponent(n.href) +
        ";" +
        Math.random(),
      o = new Image();
    o.src = i;
  } catch {}
},
```

This JavaScript code appears to be a function (`X0`) designed to send tracking data (e.g., visitor analytics) to a URL. Here's a breakdown of what it does:

### Input Parameters:

`e`: Defaults to `"t999ru"` unless provided.
`t`: A callback function or any other value passed to the function.

### Main Logic:

* Creates a new URL object (`n`) based on the current document URL.
* If `t` is a function, it invokes `t` with the `URL` object as an argument.

### Tracking URL Construction:

* The string `e` is used to customize the URL for tracking.
* Constructs a URL for a tracking endpoint (//counter.yadro.ru/hit) with the following appended data:
  * A predefined token (`t45.6`).
  * `r`: The encoded `document.referrer` (indicates the referring page).
  * `s`: Screen resolution and color/pixel depth (if available).
  * `u`: The current page's URL, encoded.
  * A random value to prevent caching.

### Sending Tracking Data:

* Creates a new `Image` object (`o`).
* Sets the `src` property of the image to the constructed tracking URL, effectively making a GET request to the endpoint.

### Error Handling:

The function is wrapped in a `try-catch` block to suppress errors if any part of the process fails (e.g., URL creation or invalid parameters).

### Purpose

This code likely implements basic visitor tracking. It collects and sends information such as:

* Referrer URL.
* Screen resolution and color depth.
* The current page URL.
* A random value for uniqueness.

### Concerns

* Privacy: It tracks user data, which might conflict with privacy regulations (e.g., GDPR).
* Security: It relies on an external endpoint without verifying responses.
* This is a typical pattern for lightweight analytics tools.
