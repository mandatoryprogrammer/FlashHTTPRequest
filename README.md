# FlashHTTPRequest

A simple Flash bridge for preforming Flash HTTP requests with JavaScript.

### Syntax
```js
FlashHTTPRequest.open( HTTP_METHOD, URI, BODY, JS_CALLBACK );
```

### Example
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8"/>
    <script src="flashhttprequest.js"></script>
    <script>
        // Ensure all FlashHTTPRequests are done via window.onload as we need to hook the Flash object
        window.onload = function() {
            FlashHTTPRequest.open('GET', 'http://example.com/', '', 'alert' );
            FlashHTTPRequest.open('POST', 'http://example2.com/POST/', 'test=test&var2=test', 'alert' );
        }
    </script>
</head>
<body>
    <div id="flashBridge"></div>
</body>
</html>
```
