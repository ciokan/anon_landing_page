# Affiliates landing page
These informations will help you customize and deploy your own landing page !

### :vertical_traffic_light: Deploy your site
- navigate to [GitHub](https://github.com) and **sign in/up**
- click the button below  
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/Alin13/landing_page)
- follow onscreen instructions:
    - Connect to GitHub - **log in** with you GitHub account
    - Configure your site - change the repository name if you want
    - wait until your site is deployed
    - click **Set up a custom domain**
    - click **Secure your site with HTTPS**
- any change you commit on GitHub after you deploy your site for the first time will trigger a build on Netlify and your site will be updated automatically

### :key: How to download the source code
- navigate to [GitHub](https://github.com) and **sign in/up**
- browse and open your repository(from the left menu) created when you clicked on **Deploy to Netlify** - or open **https://github.com/YOUR_USERNAME/PROJECT_NAME**
- click the **Clone or download** button
- from there you can **Download a ZIP** file or clone the repository using **Clone with HTTPS**
- you can then either *install & use git* on your computer or you can change the files one by one directly from your repository
- for more details, read [Help section](https://help.github.com/articles/set-up-git/)

### :star2: Change site logo and hero image
- the site logo has two versions: light (used on site enter, when the background is darker) and dark (used when the navigation bar is white - on scroll or on small devices)
    - to change the light version, save your logo to `src/images/logo600x332light.png`
    - to change the dark version, save your logo to `src/images/logo600x332dark.png`
    - keep in mind that you can use the same logo - but you must be sure that is looks ok on the both cases
    - for the best fit, try to use logos with the same size: *600x332*
- for hero image (the image that appears on the first section of the site, on the background, save the new image in `src/images/hero.png`.
    - for the best result, try to use an image with almost the same size as the original one (*1645x1398*) and transparent background.
- you can also change the favicon from `src/images/icon.png` - this is also used on mobile phones as an icon.
    - make sure that the image is big enough and square formatted, so that the quality is good everywhere.

### :rainbow: Edit site colors
- open file from `src/styles/modules/_variables.scss` and edit the variables as follows:
    - **$nav-bar-default-color** - default background color for the navigation bar
    - **$nav-bar-light-color** - background color of the navigation bar when the page is scrolled down
    - **$header-color** - color used for headings/subtitles
    - **$text-color-dark** - text color for light backgrounds
    - **$text-color-light** - text color for dark backgrounds
    - **$pricing-card-bg-color** - pricing card background color
    - **$primary-color** - the primary color - used as background for some buttons and widgets
    - **$primary-light-color** - a lighter primary color - used for some borders or effects
    - **$secondary-color** - the secondary color - used on some secondary buttons
    - **$intent-success** - success notification background color
    - **$intent-error** - error notification background color
    - **$bar-btn-hover-text-color** - hover text color for the "Buy now" button from the app bar
    - **$bar-btn-hover-bg-color** - hover background color for the "Buy now" button from the app bar
    - **$hero-gradient** - background color used in the first section of each page
    - **$footer-gradient** - background gradient used in footer
    - **$pricing-gradient** - background gradient for pricing section
    - **$sections-gradient** - background gradient for all other sections (which are not transparent)
    - **$reviews-bg-color** - background color for reviews bubbles
    - *... more details in the file*

### :hammer: Change site settings
- open file from `src/settings.js` and edit the constants as follows:
    - **SITE_URL** - your domain url
    - **SITE_NAME** - site name that appears in the footer
    - **TOS_SITE_NAME** - site/company name that appears in terms of service
    - **TOS_LAST_UPDATE** - last update of terms of service
    - **TAWK_TO_WIDGET_URL** - the link of your chat widget
    - **BACKEND_URL** - your backend services url
    - *... more details in the file*

### :telephone_receiver: Add your personal chat
- navigate to [Tawk To](https://www.tawk.to/)
- click on **Sign up** button and create a new account
- after you **sign in**, in the left menu you will find a *cog* icon with a tooltip **Admin**
- you should have a default widget which can be customized as you wish: you just have to click on **Widget Settings** and change the settings as you need
- make sure that `Hide widget on load` is checked...so that it fits the app settings
- save the settings and copy the chat link from **Widget Code**. It should look similar to this one `https://embed.tawk.to/5be5f1470ff598a7a61dba7/default`
- in `src/settings.js` paste the new link in **TAWK_TO_WIDGET_URL** constant
- you can now receive messages in the chat. You will find all your messages under the **Messages** menu
