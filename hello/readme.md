# Hello

The "Hello" app, shows the "Hello!" message in the center of the screen.  
It is made of two files `index.html`, `bg_app.jpg` and loads "jQuery" and the "Amazon Web App API" libraries.

### index.html

``` html
<html lang='en'>

<head>
    <title>Hello</title>
    <meta charset="utf-8">
    <meta id="viewport" name="viewport" content="width=device-width, initial-scale=1.0">
    <script>
        /**
         * This script will set the 'initial-scale' value on the viewport metatag
         * The scale is used to fit the template on Kindle Fire mobile devices
         * This must be handled in the head of the document because the scale
         * is not affected once the page finishes loading
         */
        var vp = document.getElementById('viewport');
        var initialScale = Math.max(screen.width, screen.height) / 1920;
        vp.setAttribute('content', 'width=device-width, initial-scale=' + initialScale + ', maximum-scale=' + initialScale, + 'minimum-scale=' + initialScale);

    </script>

    <script src="//resources.amazonwebapps.com/v1/latest/Amazon-Web-App-API.min.js"></script>
    <script src="//code.jquery.com/jquery-3.3.1.min.js"></script>

    <style>
        html,
        body {
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        body {
            position: absolute;
            padding: 0;
            margin: 0;
            font-size: 20pt;
            /* font-family: "Helvetica Neue Light", "HelveticaNeue-Light", Helvetica, Arial, sans-serif; */
            font-family: Helvetica, Arial, sans-serif;
            color: antiquewhite;
            background: #5a656f url("bg_app.jpg") no-repeat left top;
            background-size: 100% 100%;
        }

        div {
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            box-sizing: border-box;
        }

        .app-main-container {
            position: relative;
            width: inherit;
            height: inherit;
            overflow: hidden;
            font-size: 300px;
            color: aliceblue;
            text-align: center;
        }

        .vertical-align-helper {
            display: inline-block;
            height: 100%;
            vertical-align: middle;
        }
    </style>

</head>

<body>

    <div id="app-container" class="app-main-container">
        <span class="vertical-align-helper"></span>
        <span id="message" style="display: none;"></span>
    </div>

    <script>        
        
        function onAmazonPlatformReady() {
            // do something            
            $('#message').hide().html('Hello!').fadeIn(3000);
        }

        document.addEventListener("amazonPlatformReady", onAmazonPlatformReady, false);

    </script>

</body>

</html>

```
