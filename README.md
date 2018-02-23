# Adobe-OAuth-Playground
Generate an IMS OAuth access token to interact with OAuth-supported Adobe APIs


Prerequisites:

1. Access to create integrations on the [Adobe I/O Console](https://console.adobe.io).
1. Valid scopes to generate OAuth access token.
1. Code: https://github.com/adobeio/Adobe-IMS-OAuth-Playground.
1. Deploy the Adobe IMS OAuth Application on a public Node JS server (You may use Heroku for instance).


## Setup an Adobe I/O Console Integration

1. On the [Adobe I/O Console](https://console.adobe.io), click **New Integration**.


1. Click **Access an API** and then click **Continue**.

     ![access api](https://user-images.githubusercontent.com/29133525/36578831-faadb772-181c-11e8-9fbc-c9ce50a72e85.png)

1. Select services that support **OAuth Integration**. Most services support JWT access token, which can be easily generated within Adobe I/O Console Integration.



1. For **Integration Details**, provide the required information. The default redirect URI should be a public URL. For this playground app please provide the URL as https://app_address.com/handler. Once the integration is created you will see that the API Key (Client ID) and Client Secret has been generated.






## Watch It Work

Go to the URL where you have deployed the Adobe IMS OAuth application. In our case we have deployed it on Heroku: https://adobe-ims-oauth.herokuapp.com/



Copy the API Key (Client ID) from the integration created in step 6. Click on "Get Authorization Code" 
(Remove the "creative_sdk" from the scope because we didn't added it for this integration)



You will be redirected to the Adobe Sign In page. Enter your Adobe ID credentials and click on Sign In.



Upon successful sign in you will redirected to the Adobe IMS OAuth Playground application Step 2 with pre-filled "Authorization Code". 
If that is not the case then please go to your I/O Console integration and make sure that the default redirect URI is pointing to your application e.g. https://your-app-in-cloud.com/handler



Copy the "client secret" from I/O Console Integration page, paste it in Adobe IMS OAuth Playground→ Step 2→ Client Secret. Click on "Generate Access Token"



Your Adobe IMS OAuth access token and refresh token are generated successfully!




