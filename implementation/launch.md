# Adobe Launch Implementation Guide

The embed code is a <script> tag that you put on your webpages to load and execute the logic you build in Launch. If you load the library asynchronously, the browser continues to load the page, retrieves the Launch library, and executes it in parallel. In this case, there is only one embed code, which you put in the `<head>` (When Launch is deployed synchronously, there are two embed codes, one which you put in the <head> and another which you put before the </body> ).

From the property Overview screen, click on the Environments tab to go to the environments page (Note that Development, Staging, and Production environments have been pre-created for you):
    
![Environments screen](https://docs.adobe.com/content/dam/help/core-services-learn.en/help/website-implementation/images/launch-environments.png)

Development, Staging, and Production environments correspond to the typical environments in the code development and release process. Code is first written by a developer in a Development environment. When they have completed their work, they send it to a Staging environment for QA and other teams to review. Once the QA and other teams are satisfied, the code is then published to the Production environment, which is the public-facing environment which your visitors experience when they come to your website.

Launch permits additional Development environments, which is useful in large organizations in which multiple developers are working on different projects at the same time.

These are the only environments we need to complete the tutorial. Environments allow you to have different working versions of your Launch libraries hosted at different URLs, so you can safely add new features and make them available to the right users (e.g. developers, QA engineers, the public, etc.) at the right time.

Now, let's copy the embed code:
1. In the Development row, click the Install icon  to open the modal.
2. Note that Launch will default to the asynchronous embed codes
3. Click the Copy icon  to copy the embed code to your clipboard.
4. Click Close to close the modal.

![Web Install Instructions](https://docs.adobe.com/content/dam/help/core-services-learn.en/help/website-implementation/images/launch-copyInstallCode.png)


## Implement the Embed Code in the <head> of the Sample HTML Page

The embed code should be implemented in the <head> element of all HTML pages that will share the property. You might have one or several template files which control the <head> globally across the site, making it a straightforward process to add Launch.

```html
<!--Launch Header Embed Code: REPLACE LINE 39 WITH THE EMBED CODE FROM YOUR OWN DEVELOPMENT ENVIRONMENT-->
<script src="<your_library_url>" async></script>
<!--/Launch Header Embed Code-->
```

Make sure you build a version of the library and then test that the JS file is correctly loading on the page.

For more information refer to the [official documentation](https://docs.adobe.com/content/help/en/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch.html).