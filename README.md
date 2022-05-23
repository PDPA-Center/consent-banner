# Cookies Consent Banner
Frontend banner dialog for user to consent cookies

DEMO : https://donjaimediaplus.com/demo/cc/

## How to Installation
1. Clone folder to your project

2. Import the stylesheet: add a `stylesheet` tag on `<HEAD>` and pointing to `cookieconsent.css`

    ```html
    <link rel="stylesheet" href="assets/style/cookieconsent.css">
    ```

3. Import the script: add a `script` tag before closing `</BODY>` and pointing to `cookieconsent.js`

    ```html
    <html>
        <head> <!-- head content --> </head>
        <body>
            <!-- body content -->
          
            <script defer src="assets/js/cookieconsent.js"></script>
        </body>
    </html>
    ```

4. Import the script: add a `script` tag before closing `</BODY>` and pointing to `cookieconsent-init.js`

    ```html
    <html>
        <head> <!-- head content --> </head>
        <body>
            <!-- body content -->
          
            <script defer src="assets/js/cookieconsent.js"></script>
            <script defer src="assets/js/cookieconsent-init.js"></script>
        </body>
    </html>
    ```
    
5. Insert the HTML button: add a `button` tag before script on 3. & 4.

    ```html
    <html>
        <head> <!-- head content --> </head>
        <body>
            <!-- body content -->
          
            <button id="cc-reconsent" data-cc="c-settings">ตั้งค่าคุกกี้</button>
          
            <script defer src="assets/js/cookieconsent.js"></script>
            <script defer src="assets/js/cookieconsent-init.js"></script>
        </body>
    </html>
    ```
    
6. Custom your setting on `cookieconsent-init.js`
7. Custom your theme on `assets/style/cookietheme.css`


## How to define cookiecategory
From the specifications, we will categorize cookies into 4 types:
1. necessary
2. functional
3. analytical
4. marketing

## How to block/manage scripts
1. Set `type="text/plain"` and `data-cookiecategory="<category>"` to any `script` tag you want to manage:

    ```html
    <script type="text/plain" data-cookiecategory="marketing" src="marketing.js" defer></script>

    <script type="text/plain" data-cookiecategory="functional">
        console.log('"functional" category accepted');
    </script>
    
    <script type="text/plain" data-cookiecategory="analytical" async src="https://www.googletagmanager.com/gtag/js?id=UA-00000000-0"></script>
	<script type="text/plain" data-cookiecategory="analytical">
        window.dataLayer=window.dataLayer||[];
        function gtag(){dataLayer.push(arguments);}
        gtag('js',new Date());
        gtag('config','UA-00000000-0');
    </script>
    ```
    <i>Note: `data-cookiecategory` must be a valid category defined inside the configuration object</i>

2. Testing!

## How to know what's technologies on your web
Install `Wappalyzer` chrome extension: https://www.wappalyzer.com/













