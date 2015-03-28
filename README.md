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
        // This function will be called when the Flash bridge has been loaded
        // Note that you can only request from sites that allow you to via their /crossdomain.xml policy
        function onhook() {
                FlashHTTPRequest.open('GET', 'http://www.example.com/', '', 'alert' );
                FlashHTTPRequest.open('POST', 'http://www.example.com/', 'var1=test&var2=test2', 'post_receiver' );
        }

        // Response data is passed as an argument to the callback defined
        function post_receiver( response ) {
            console.log( response );        
        }
        </script>
</head>
<body>
        <div id="flashBridge"></div>
</body>
```
