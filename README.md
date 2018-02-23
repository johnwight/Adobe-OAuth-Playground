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

     ![launch integration](https://user-images.githubusercontent.com/29133525/36612482-ef4ef464-1893-11e8-9f3a-63c808659d48.png)


1. For **Integration Details**, provide the required information. The default redirect URI should be a public URL. For this playground app please provide the URL as https://app_address.com/handler. Once the integration is created you will see that the API Key (Client ID) and Client Secret has been generated.

     ![integration details](https://user-images.githubusercontent.com/29133525/36612561-341c3494-1894-11e8-8241-c3a2791511a7.png)


## Watch It Work

1. Go to the URL where you have deployed the Adobe IMS OAuth application. In our case we have deployed it on Heroku: https://adobe-ims-oauth.herokuapp.com/.



1. Copy the API Key (Client ID) from the integration you previously created. Click **Get Authorization Code** Remove the **creative_sdk** text from the scope because we did not add it for this integration.



1. After you are redirected to the Adobe Sign In page, enter your Adobe ID credentials and click **Sign In**.



1. Upon successful sign in you are redirected to the Adobe IMS OAuth Playground application Step 2, with a pre-filled **Authorization Code**. If that is not the case, return to your I/O Console integration and make sure that the default redirect URI is pointing to your application (https://your-app-in-cloud.com/handler).



1. Copy the **client secret** from the I/O Console Integration page, paste it in Adobe IMS OAuth Playground > Step 2 > Client Secret. Click **Generate Access Token**.



Your Adobe IMS OAuth access token and refresh token are generated successfully!



## Feedback?

Please help make this solution as useful as possible. If you find a problem in the documentation or have a suggestion, click the **Issues** tab on this GiHhub repository and then click the **New issue** button. Provide a title and description for your comment and then click the **Submit new issue** button.

   ![submit new issue](https://user-images.githubusercontent.com/29133525/32515298-f344bd5a-c3bc-11e7-9978-34516f964f9f.png)


