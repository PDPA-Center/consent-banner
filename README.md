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
    
5. Insert the HTML button: add a `button` tag before script on 3 & 4

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

## How to block/manage scripts
Set `type="text/plain"` and `data-cookiecategory="<category>"` to any `script` tag you want to manage:

    ```html
    <script type="text/plain" data-cookiecategory="analytical" src="analytics.js" defer></script>

    <script type="text/plain" data-cookiecategory="functional">
        console.log('"functional" category accepted');
    </script>
    ```
    
<i>Note: `data-cookiecategory` must be a valid category defined inside the configuration object</i>
















