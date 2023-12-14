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