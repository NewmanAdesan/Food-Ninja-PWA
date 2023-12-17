- when we select an html file, 
- it opens the file in a browser using the 'file protocol' that is sth like C:/Users/.../index.html
- but when using progressive web application technologies we need to serve our pages using the 'http protocol'
- so we have to use a local development server to open our html file in the browser.


- Link to Material CSS, JS, Icons
- Linkt to Extenal CSS


- Create a WebApp Manifest File (provide information about our app to the browser)
    - 'name property' to 'Food Ninja': 
            - shows when you click on the application on a splash screen when the application loads on a mobile.
    - 'short_name property' to 'FoodNinja': 
            - name that displays underneath the icon on the homescreen when someone installs the application
    - 'start_url property' to '/index.html': 
            - page that loads up when the user taps on the icon when app is install unto the homescreen. 
    - 'display property' to 'standalone': 
            - standalone means i want the app to look like native app when it opens. here it wont show all the browser things in the application, things like the address bar at the top because it would look like a native app
            - browser means when the user tap the icon its going to open up the application in a much like google chrome. 
    - 'background_color' to '#FFE9D2':
            - this dictates the background of the spash scrren when we first load the application
    - 'theme_color' to 'FFE1C4':
            - the colorize the little bar at the top of the application.
    - 'orientation to 'portrait-primary':
            - the orientation the app opens
    - 'icons' which is an array of different sized icons so that depending on the device you are running the app on, it would pick a particular icon. the array is an object with 3 keys 'src', 'type', 'sizes'
        - src to '/img/icons/icon-384x384.png'
        - type to 'image/png'
        - sizes to '512x512'
- Link to the Manifest File from our index.html file
- the point of this is to tell the browser information about the application so that when it is displayed on the homescreen, it loads correctly.



Previewing in an android emulation
        - download android studio and spin up an android emulator
        - open up google chrome on the device & use a proxy link to view website
        - (not 127.0.0.1:5500/index.html) as in your browser
        - (but rather 10.0.2.2:5500) and we should see our website
        - in chrome browser, click on the hamburger icon and choose 'Add to homescreen'.
        - on the homescreen you should see the app that can be loaded and the view will be like a native app. 
        - notice the url bar is not present. this is because of the display property in our manifest.json



IOS SUPPORT
        - some of the manifest property are not supported on IOS namely the icons & theme_color.
        - if we tried to add this app using safari on an IOS device, it will not use the icons that we specify instead it will take a screen shot of our app and use that as the icon instead
        - to set the icon, we would use a link element in the head of our html to set the icon to use on apple devices. (we could use multiple link element for each size to the IOS device can choose one)
                <link rel="apple-touch-icon" href="img/icons/icon-96x96.png" />
        
        - to set the theme-color, we would use a meta tag
                <meta name="apple-mobile-web-app-status-bar" content="#aa7700" />

            "src": "img/icons/icon-96x96.png